**The profile with the id set to `1` will be the default terminal.**

_The profiles will only function, if the corresponding terminals are installed. Starting in v0.9.2, Files UWP will automatically detect if Windows terminal and Fluent Terminal are installed._

cmd:
```
{
      "name": "CMD",
      "path": "cmd.exe",
      "arguments": "/k \"cd /d {0} && title Command Prompt\"",
      "icon": ""
}
```
Powershell:
```
{
      "name": "PowerShell",
      "path": "powershell.exe",
      "arguments": "-noexit -command \"cd '{0}'\"",
      "icon": ""
}
```
Powershell Core:
```
{
      "name": "PowerShell Core 6",
      "path": "pwsh.exe",
      "arguments": "-WorkingDirectory \"{0}\"",
      "icon": ""
}
```
Windows Terminal:
```
{
      "name": "Windows Terminal",
      "path": "wt.exe",
      "arguments": "-d \"{0}\"",
      "icon": ""
}
```
Fluent Terminal:
```
{
      "name": "Fluent Terminal",
      "path": "flute.exe",
      "arguments": "new \"{0}\"",
      "icon": ""
}
```