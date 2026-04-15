# AzureChina-O365-Password-Spray-
AzureChina/O365 Password Spray via https://login.partner.microsoftonline.cn

## Quick Start
You will need a userlist file with target email addresses one per line. Open a PowerShell terminal from the Windows command line with 'powershell.exe -exec bypass'.

```PowerShell
Import-Module MSOLSpray.ps1
Invoke-MSOLSpray -UserList .\userlist.txt -Password Winter2020
```

### Invoke-MSOLSpray Options
```
UserList  - UserList file filled with usernames one-per-line in the format "user@domain.com"
Password  - A single password that will be used to perform the password spray.
OutFile   - A file to output valid results to.
Force     - Forces the spray to continue and not stop when multiple account lockouts are detected.
URL       - The URL to spray against. Potentially useful if pointing at an API Gateway URL generated with something like FireProx to randomize the IP address you are authenticating from.
```
