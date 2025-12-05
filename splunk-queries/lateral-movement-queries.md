FOR SMB ENUMERATION ACTIVITY
index=windows_logs EventCode=5140 OR EventCode=5145
| stats count by src_ip, dest_ip
| where count > 50
| table src_ip, dest_ip, count
