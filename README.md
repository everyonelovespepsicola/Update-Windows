# Update-Windows
Update Winows Command Line

To install Windows updates via PowerShell, you need to install the module first:
Install-Module PSWindowsUpdate
Add-WUServiceManager -MicrosoftUpdate

Show available updates
Get-WindowsUpdate

install the specific KB
Install-WindowsUpdate -KBArticleID KBxxxxxxx -AcceptAll

Install all available updates 

Install-WindowsUpdate -MicrosoftUpdate -AcceptAll -AutoReboot | Out-File "C:\($env.computername-Get-Date -f yyyy-MM-dd)-MSUpdates.log" -Force
