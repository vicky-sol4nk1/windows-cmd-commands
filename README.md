# windows-cmd-commands
cmd commands for managing process

| Purpose                   | Command                        | Example                                 |
| ------------------------- | ------------------------------ | --------------------------------------- |
| List all processes        | `tasklist`                     | `tasklist`                              |
| Filter process by name    | `tasklist \| findstr name`     | `tasklist \| findstr chrome`            |
| Show detailed info        | `tasklist /V`                  | `tasklist /V`                           |
| Show services per process | `tasklist /SVC`                | `tasklist /SVC`                         |
| Kill process by name      | `taskkill /IM name.exe`        | `taskkill /IM chrome.exe`               |
| Force kill process        | `taskkill /F /IM name.exe`     | `taskkill /F /IM chrome.exe`            |
| Kill process by PID       | `taskkill /PID PID`            | `taskkill /PID 1234`                    |
| Kill process tree         | `taskkill /T /PID PID`         | `taskkill /T /PID 1234`                 |
| Kill multiple processes   | `taskkill /IM a.exe /IM b.exe` | `taskkill /IM notepad.exe /IM calc.exe` |
| Start a process           | `start program`                | `start notepad`                         |
| Start minimized           | `start /MIN program`           | `start /MIN notepad`                    |
| Open Resource Monitor     | `resmon`                       | `resmon`                                |
| Open Performance Monitor  | `perfmon`                      | `perfmon`                               |



# powershell commands for process managment

| Purpose                | Command                             | Example                                                     |
| ---------------------- | ----------------------------------- | ----------------------------------------------------------- |
| List all processes     | `Get-Process`                       | `Get-Process`                                               |
| Get process by name    | `Get-Process -Name name`            | `Get-Process chrome`                                        |
| Get process by PID     | `Get-Process -Id PID`               | `Get-Process -Id 1234`                                      |
| Detailed process info  | `Get-Process \| Format-List *`      | `Get-Process chrome \| fl *`                                |
| Sort by CPU usage      | `Get-Process \| Sort CPU -Desc`     | `Get-Process \| Sort CPU -Desc`                             |
| Stop process by name   | `Stop-Process -Name name`           | `Stop-Process chrome`                                       |
| Force stop process     | `Stop-Process -Name name -Force`    | `Stop-Process chrome -Force`                                |
| Stop process by PID    | `Stop-Process -Id PID`              | `Stop-Process -Id 1234`                                     |
| Start process          | `Start-Process program`             | `Start-Process notepad`                                     |
| Start as administrator | `Start-Process program -Verb RunAs` | `Start-Process cmd -Verb RunAs`                             |
| Wait for process       | `Wait-Process -Name name`           | `Wait-Process notepad`                                      |
| Get parent process     | `Get-CimInstance Win32_Process`     | `Get-CimInstance Win32_Process`                             |
| Show command line      | `Select Name, CommandLine`          | `Get-CimInstance Win32_Process \| Select Name, CommandLine` |
