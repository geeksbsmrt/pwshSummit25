# Lightning Demos

Speakers: Random
Room: 404
Time: 15:30 - 17:00

## Session Description

BYO ideas! 5 mins or less.

## Notes

- AppLockerTempRules
  - Creates temporary AppLockerRules
  - Looks at EventLog and can temporarilly allow bypass of AppLocker Restrictions
- Get-PesterRequiredVersion
  - Jane Street internally developed module that parses Pester files via AST to get the version necessary
  - We should standardize on 5
- Gilbert Sanchez - Resume as Code:
  - JSONResume.org
    - Custom Schema
  - Share resume as GIST, it will host for you
  - Supports theming
  - Keep everything in it and build role specific to print\export
- Microsoft Artifact Registry
- Task Config Files
  - PowerShell Data files `.psd1` file
    - Hashtable written to disc as text
    - Used to describe a Scheduled Task
    - `Import-PowerShellDataFile -Path -OutVar`
- DSC v3
  - Bicep
  - Winget
- David Whittaker - Modules
  - PoSh Markdown - Outputs PSObjects into Markdown
  - PSModuleScaffodling
- AnyPackage
  - Supports multiple Package Providers and is cross-platform
- PowerShell `filter` keyword
  - Takes a`scriptblock` sets it as `process` as default instead of `end`
  - PowerShell 7.5 errors have Recommended Action Output
- PSScripAnalyzer Custom Rules
  - Uses AST inspection
