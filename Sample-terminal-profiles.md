**The profile with the id set to `1` will be the default terminal.**

_The PowerShell 6 and the Windows Terminal profile will only function, if the corresponding terminals are installed._

cmd:
```
{
      "id": 1,
      "name": "CMD",
      "path": "cmd.exe",
      "arguments": "/k \"cd /d {0} && title Command Prompt\"",
      "icon": ""
}
```
Powershell:
```
{
      "id": 2,
      "name": "PowerShell",
      "path": "powershell.exe",
      "arguments": "-noexit -command \"cd '{0}'\"",
      "icon": ""
}
```
Powershell Core:
```
{
      "id": 3,
      "name": "PowerShell Core 6",
      "path": "pwsh.exe",
      "arguments": "-WorkingDirectory \"{0}\"",
      "icon": ""
}
```
Windows Terminal:
```
{
      "id": 4,
      "name": "Windows Terminal",
      "path": "wt.exe",
      "arguments": "-d \"{0}\"",
      "icon": ""
}
```
Fluent Terminal:
```
{
      "id": 5,
      "name": "Fluent Terminal",
      "path": "flute.exe",
      "arguments": "new \"{0}\",
      "icon": ""
}
```