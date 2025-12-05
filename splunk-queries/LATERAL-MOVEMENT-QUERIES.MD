net.exe
index=endpoint process_name="net.exe"
| search command_line="*view*" OR command_line="*use*"
| stats count by host, user, command_line
| where count > 20
