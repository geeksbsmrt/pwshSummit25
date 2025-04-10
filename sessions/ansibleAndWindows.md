# Ansible and Windows. How PowerShell enables a Linux config manager to work in a Windows world?

Speaker: Paul Broadwith
Room: 406
Time: 1:50 - 2:35

## Session Description

Ansible is a Linux based configuration manager. So how does a Linux based configuration manager manage Windows?

Using our beloved PowerShell of course.

In this talk I'll discuss how a Linux based configuration manager can manage Windows, how it manages Windows and some trick and tips on using it successfully (psst, it's because PowerShell).

## Notes

- OpenSSH 7.9.0 is the only officially supported OpenSSH, can use WinRM.
- Don't use Write-Host\Debug\Verbose\Error in Ansible PwSh scripts
