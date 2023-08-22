# Windows Local Administrator Password Solution (Windows LAPS)
- [x] Research
- [ ] Testing
- [ ] Draft
- [ ] Completed

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

- [Window Event Collector](#Window-Event-Collector)
- [Window Event Logging](#Window-Event-Logging)
- [SYSMON-Logging](#SYSMON)
- [DNS Logging](#DNS-Logging)
