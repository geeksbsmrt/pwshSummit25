# The Incredible Extensible PSObject

Speaker: James Brundage
Room: 406
Time: 14:35 - 15:00

## Session Description

You might think you understand PowerShell, but do you know all that you can know about PSObjects?

In this talk, we'll cover some of the interesting aspects of PowerShell objects you might not be aware of. We'll show how you can easily extend any object to do anything you need it to and how to make objects you couldn't possibly create in C#.

We'll see why PSObjects are much more powerful than their compiled counterparts, and how that opens doors for us all.

## Notes

- Start-Automating
- PSObject:
  - Properties can be anything
  - As can types
- Fast way `$object.psobject.menmbers.add`
- Create in `[ordered]` and cast to `[PSCustomObject]`
- Update-TypeData
  - `.types.ps1xml` is faster but not easily debuggable
- Extending MD
  - Get-TypeData -Name $TypeName
- PSObjects are Dynamically Polymorphic
  - They can 'shapeshift'

### Resources

- EZOut
