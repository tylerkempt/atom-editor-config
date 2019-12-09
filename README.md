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
5. Open Atom: *File > Settings > Packages > Sync Settings > Settings*
    - Personal Access Token: (*GitHub: Account settings > Developer settings > Personal access tokens > Generate new token with 'Gist' scope*)
    - Gist ID: (*Copy ID from previously created secret Gist*)

------------

## Troubleshooting

#### `apm` is not a recognized as an internal or external command, operable program or batch file.
**Issue**: Atom is likely not part of your user or system path. To verify:
```
C:\> echo %PATH%
```

**Solution**: Add Atom editor to your system path:
```
C:\> echo %PATH% > %USERPROFILE%\Desktop\path-backup.txt
C:\> setx /M path "%PATH%;%LOCALAPPDATA%\atom\bin"
```
See: https://discuss.atom.io/t/installing-apm-on-windows-am-i-missing-something/13089/10


