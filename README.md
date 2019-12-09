# atom-editor-config

## About
My personal configuration for GitHub Atom editor.

## Prerequisites

 - **Operating System**: Windows 10
 - **Package Management**: Chocolatey ([https://chocolatey.org/](https://chocolatey.org/))
 
## Setup

From an elevated command prompt or PowerShell window:

1. Install Atom Editor: 
`choco install atom -y`
2. Refresh your environment variables to register `atom` and `apm` to your PATH:
`refreshenv`
3. Install fonts:
`choco install hackfont firacode inter -y`
4. Install Atom [sync-settings](http://https://atom.io/packages/sync-settings "sync-settings") package:
`apm install sync-settings`

## Troubleshooting

#### `apm` is not a recognized as an internal or external command, operable program or batch file.
**Issue**: Atom is likely not part of your user or system path. To verify:
```
C:\> echo %PATH%
```

**Solution**: Add Atom editor to your system path:
```
C:\> echo %PATH% > %USERPROFILE%\Desktop\path-backup.txt
C:\> setx /M path "%PATH%;%LOCALAPPDATA%\atom\atom.exe"
```


