# atom-editor-config

## About
My personal configuration for GitHub Atom editor.

## Prerequisites

 - **Operating System**: Windows 10
 - **Package Management**: Chocolatey ([https://chocolatey.org/](https://chocolatey.org/))
 
## 📦 Setup

From an elevated command prompt or PowerShell window:

1. Install GitHub Atom editor: 
`choco install atom -y`
2. Refresh your environment variables to register `atom` and `apm` to your PATH:
`refreshenv`
3. Install required fonts:
`choco install hackfont firacode inter -y`
4. Install Atom [sync-settings](http://https://atom.io/packages/sync-settings "sync-settings") package:
`apm install sync-settings`
5. Open Atom: *File > Settings > Packages > Sync Settings > Settings*
    - **Personal Access Token**: Generate a new token with the 'Gist' scope (*GitHub: Account settings > Developer settings > Personal access tokens > Generate new token*)
    - **Gist ID**: Copy ID from secret Gist previously created
6. Close and reopen Atom editor.
7. You should be presented with a warning: "sync-settings: Your settings are out of date." Click **Restore**
8. Once Sync Settings finishes installing all packages/settings, close and reopen Atom editor

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


