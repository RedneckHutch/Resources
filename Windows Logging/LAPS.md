# Windows Local Administrator Password Solution (Windows LAPS)

# What is it used for?
LAPS is used for automatically managing and backs up the password of a local administrator account, both on Azure Activer directory or Window Server active directory. It can also be used for automatically backing up and restoring the Directory Services Restore Mode (DSRM) account password of on domain controllers.

# Why is this usesful?
Authorized system adminstrators are able to retrieve these passwords if needed.

# Benefits 
- Protection against pass-the-hash and lateral-traversal attacks
- Improved security for remote help desk scenarios
- Ability to sign in to and recover devices that are otherwise inaccessible
- A fine-grained security model (access control lists and optional password encryption) for securing passwords that are stored in Windows Server Active Directory
- Support for the Azure role-based access control model for securing passwords that are stored in Azure Active Directory

# How to see if it is installed?
When the LAPS client is installed, the Group Policy Client Side Extension (CSE) is configured on the computer. This is a DLL (admpwd.dll) located in c:\program files\LAPS\CSE and is configured in the registry: HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Winlogon\GPExtensions.

Using PowerShell, we can check for the presence of the DLL:
```Get-ChildItem 'c:\program files\LAPS\CSE\Admpwd.dll'``` or ```Get-ChildItem 'C:\Program Files (x86)\LAPS\CSE\Admpwd.dll'```
Using PowerShell v5, we can check the file hash & hashing algorithm on the DLL:
```Get-FileHash 'c:\program files\LAPS\CSE\Admpwd.dll'```

Using PowerShell v5, we can check the digital signature on the DLL:
```Get-AuthenticodeSignature 'c:\program files\LAPS\CSE\Admpwd.dll'```
