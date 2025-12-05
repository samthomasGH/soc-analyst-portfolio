IMPOSSIBLE TRAVEL QUERY
index=azuread sourcetype="azure:ad:signin"
| eval geo_pair = src_country . " -> " . dest_country
| stats earliest(_time) as first_login latest(_time) as second_login by user, geo_pair
| where first_login + 900 < second_login  /* 15 minutes threshold */
| table user, geo_pair, first_login, second_login
====================
PASSWORD SPRAY DETECTION
index=auth_logs ("Invalid password" OR "authentication failed")
| stats count by src_ip, user
| where count > 5
| stats dc(user) as unique_users, sum(count) as total_attempts by src_ip
| where unique_users > 10
