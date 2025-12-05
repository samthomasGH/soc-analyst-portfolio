index=edr_processes process_name="powershell.exe"
| search command_line="*EncodedCommand*" OR command_line="*Base64*"
| table _time, host, user, parent_process, command_line
