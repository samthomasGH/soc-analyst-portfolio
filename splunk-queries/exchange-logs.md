PHSHING DETECTION
index=o365 sourcetype="o365:messageTrace"
| search Subject="*SharePoint*" AND SenderDomain!="microsoft.com"
| stats count dc(Recipient) as unique_recipients values(Url) as urls by SenderAddress, Subject
