# PowerShell for Pure Productivity and Perhaps Profit

Speakers: Andrew Pla & James Ruskin
Room: 404
Time: 9:00 - 9:25

## Session Description

In this session, we'll walk you through what we think of as our secret sauce - the stuff that makes us more productive (and prettier), be that additions to our profiles, must-have modules, PSReadLine customisation, and even more!
Though we've got nothing secretive to show, you'll find a few hints and tips that improve your day to day workflow - helping you get more stuff done, more quickly.

## Notes

- $Profile.CurrentUserAllHosts, $Profile.CurrentUserCurrentHost ($AllUsers...)
  - Hosts are console hosts, not machine hosts (VSCode, pwsh.exe, powershell.exe, etc...)
- Can add secretmanagement calls
  - Do not hardcode secrets
- Can support multiple OS types
- Easier to put somethi9ng in the Profile than a module if you want it always avil.
- Update Methods on Types
- Add better views to Types
- PSReadLine
  - Module Install Dir contains sample profile
  - Get-PSReadLineKeyHandlers
    - `-Bound` to see all configured
    - Can bind to `Enter`
  - CTRL+Space displays all potential options in completions
  - Get-PSReadlineOption
  - F1 - Runs help for current command.
    - Q to go back
  -
- F7 History Module changes PSReadLine gives a UI List of historical commands
- FancyClearHost
  - Provides cool animations when clearing console
- Profiler
  - Trace-Script
- Hosting Profiles - ChezMoi, Git
