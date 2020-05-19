In order to add an option to launch Files UWP to the File Explorer right-click context menu you need to install an `inf` file. It is simple to undo any changes made by uninstalling the `inf` file using Control Panel. This feature is completely optional and not necessary for the app to run.

To get started, create a blank file called `filesuwphere.inf`. Next copy and paste the code below into the file. Once you did that, save the file and then from Files Explorer, right-click on `filesuwphere.inf` and click install.

```
; "Files UWP" PowerToy

[version]
signature="$CHICAGO$"

[FilesUWPHereInstall]
CopyFiles = FilesUWP.Files.Inf
AddReg    = FilesUWPHere.Reg

[DefaultInstall]
CopyFiles = FilesUWP.Files.Inf
AddReg    = FilesUWPHere.Reg

[DefaultUnInstall]
DelFiles  = FilesUWP.Files.Inf
DelReg    = FilesUWPHere.Reg

[SourceDisksNames]
55="Files UWP Here","",1

[SourceDisksFiles]
FilesUWPHere.INF=55

[DestinationDirs]
FilesUWP.Files.Inf = 17

[FilesUWP.Files.Inf]
FilesUWPHere.INF

[FilesUWPHere.Reg]
HKLM,%UDHERE%,DisplayName,,"%FilesUWPHereName%"
HKLM,%UDHERE%,UninstallString,,"rundll32.exe syssetup.dll,SetupInfObjectInstallAction DefaultUninstall 132 %17%\FilesUWPHere.INF"
HKCR,Directory\Shell\FilesUWPHere,,,"%FilesUWPHereAccel%"
HKCR,Directory\Shell\FilesUWPHere,Icon,,"%FilesUWPHereIcon%"
HKCR,Directory\Shell\FilesUWPHere\command,,0x00020000, "%%LOCALAPPDATA%%\Microsoft\WindowsApps\files.exe -Directory" ""%1""
HKCR,Directory\Background\Shell\FilesUWPHere,,,"%FilesUWPHereAccel%"
HKCR,Directory\Background\Shell\FilesUWPHere,Icon,,"%FilesUWPHereIcon%"
HKCR,Directory\Background\Shell\FilesUWPHere\command,,0x00020000, "%%LOCALAPPDATA%%\Microsoft\WindowsApps\files.exe -Directory" ""%V""
HKCR,Drive\Shell\FilesUWPHere,,,"%FilesUWPHereAccel%"
HKCR,Drive\Shell\FilesUWPHere,Icon,,"%FilesUWPHereIcon%"
HKCR,Drive\Shell\FilesUWPHere\command,,0x00020000, "%%LOCALAPPDATA%%\Microsoft\WindowsApps\files.exe -Directory" ""%1\""

[Strings]
FilesUWPHereName="Files UWP Here PowerToy"
FilesUWPHereAccel="Open Files UWP Here"
UDHERE="Software\Microsoft\Windows\CurrentVersion\Uninstall\FilesUWPHere"
FilesUWPHereIcon=""%%LOCALAPPDATA%%\Microsoft\WindowsApps\files.exe",0"
```