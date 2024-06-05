**** How to update Windows 10 using command Prompt as Administrator ****

### Updating Windows 10 using Command Prompt (CMD) can be done by leveraging Windows Update commands. Here’s a step-by-step guide:

#### Method 1: Using wuauclt Commands

Open Command Prompt as Administrator:

```sh
Press Win + X and select Command Prompt (Admin) or Windows PowerShell (Admin).
```

Execute Update Commands:

Type the following commands one by one and press Enter after each:

```sh
wuauclt /detectnow
wuauclt /updatenow
```

The wuauclt commands will instruct Windows to check for updates and install them if available.

Method 2: Using usoclient Commands

Open Command Prompt as Administrator:

```sh
Press Win + X and select Command Prompt (Admin) or Windows PowerShell (Admin).
```

Execute Update Commands:

Type the following commands one by one and press Enter after each:

```sh
usoclient StartScan
usoclient StartDownload
usoclient StartInstall
usoclient RefreshSettings
```

These usoclient commands initiate a scan for updates, download them, and install them.

Method 3: Using PowerShell Commands

Open PowerShell as Administrator:

```sh
Press Win + X and select Windows PowerShell (Admin).
```

Execute Update Commands:

Type the following PowerShell script and press Enter:

```sh
Install-Module PSWindowsUpdate
Import-Module PSWindowsUpdate
Get-WindowsUpdate
Install-WindowsUpdate
```

This script uses the PSWindowsUpdate module to check for and install updates.

#### Notes:
Restart Requirement: Some updates may require a system restart. You can trigger a restart using the following command:

```sh
shutdown /r /t 0
```

Administrator Privileges: Running Command Prompt or PowerShell as an administrator is crucial for these commands to execute successfully.

These methods should help you manage Windows updates directly through the command line, providing a more automated and scriptable approach.

#################################################

Open Command Prompt as Administrator:   (Window + S)

```sh
winget upgrade
```

It will scan and update outdated software on windows.

```sh
winget upgrade --all
```

It will scan and update all the software along with outdated software as well.
