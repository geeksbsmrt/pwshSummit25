# PowerShell Performance and Technique Tweaks: The Encore

| Room | Time | Speaker |
|------|------|---------|
| 401  | 13:00 - 14:30 | Christian Ritter |

## Session Description

Last year, I presented "PowerShell Performance and Technique Tweaks: The Full Show," where we explored ways to enhance your code’s performance and uncovered advanced PowerShell techniques that you may not have been familiar with. This year, I’m excited to bring you an encore, delving into new topics to expand your PowerShell toolkit.

In this session, we’ll cover:

View formatting using XML files
Best practices for storing data within your code or modules
Why extending an array is no longer as inefficient as it once was
The power of Smart Aliases
Passing data between different runspaces
This session is ideal for those who enjoyed last year’s presentation, but it’s equally valuable for anyone new who wants to learn fresh techniques for tackling PowerShell challenges in innovative ways. Whether or not you attended last time, you’ll gain insights to improve both your code and problem-solving approach.

And for everyone who is asking, yes there will be kittens again :)

## Notes

- Smart Aliasing
  - Get-API(User\Device\Application)
  - Get-APIResource
    - Use Param with ValidateSet
    - Use multiple `Alias` and build logic
      - `$MyInvocation.MyCommand.Name` - Defined function
      - `$MyInvocation.InvocationName`
        - Parse `$MyInvo.MyCom.Name` out
    - Store Resource Names in array, loop, add new alias
  - Dynamic Parameters
    - Referenced in code via `hastable` accessor: `$PSBoundParameters['ParamName']`
    - `$ParamName` will not be defined.
- FormatView
  - Add to PSProfile to have constant
  - New-PSFormatXML - PSScriptTools from Jeff Hicks
  - Update-FormatData *.psm1xml
  - Format-Table -View ViewName
  - When multiple views are defined, array[0] is the selected view
  - Update-FormatData -PrependPath
- Out-Null performance degredation resolved in Pwsh 7.3
- PowerShell Runspaces
  - Global variables not shared
    - If you attempt to change a Global variable inside a Runspace, it will not update parent scope
  - Create external class
- Module Data
  - FrozenDictionaries are immutable
- Linq
  - .Where is faster than | Where-Object
- `[ref]`
  - Allows updating primative variables without passing object around
