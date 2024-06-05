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
