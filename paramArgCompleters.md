# Pimp Your Parameters: The Magic of PowerShell Argument Completers

Speaker: Emrys MacInally
Room: 405
Time: 13:00 - 13:45

## Session Descriptiopn

Ever wondered how PowerShell sometimes knows exactly what values to suggest when you hit Tab? Want your custom functions to feel as polished as native cmdlets? This session dives into the world of argument completers – the secret sauce behind intelligent parameter suggestions in PowerShell.
Learn how to transform your functions from basic scripts into professional-grade tools that anticipate user needs and guide them through parameter selection. We'll explore practical examples of argument completers that can suggest files, processes, cloud resources, and custom values. By the end of this session, you'll understand how to implement this "black magic" in your own functions, making them more intuitive and user-friendly.

## Notes

- `ValidateSet` is the most basic Arg Completer
  - It only works for a pre-known set of values
- `enum` operates similarly
- Bad: `ArgumentCompleter({'','',''})`
  - This is basically ValidateSet without input validation
  - Does NOT respect partial inputs during lookups
- Better:
  - `ArgumentCompletions('','','')`
    - Will give full list of avail options when pressing Tab
    - Respects partial inputs during lookups
    - Does not perform input validation
  - `ArgumentCompleter({Get-Service | Select -Exp Name})`
    - Returns dynamic list of acceptible values from the ScriptBlock
    - Does not perform Input validation
    - Does not respect partial input
  - `ArgumentCompleter({Get-Service | Select -Exp Name | %{ [System.Management.Automation.CompletionResult]::new($_<#DisplayName#>, $_<#Value#>, 'ParameterValue', 'ToolTip Text')}})`
    - Does not respect partial input
    - Does not perform input validation
  -

  ```powershell
  ArgumentCompleter({
    param($commandName, $parameterName, $wordToComplete, $commandAst, $fakeBoundParameters)
    Get-Service | Select -Exp Name | ? {$_ -like "*$wordToComplete*"} | %{ [System.Management.Automation.CompletionResult]::new($_<#DisplayName#>, $_<#Value#>, 'ParameterValue', 'ToolTip Text')}
    })
  ```

  - $fakeBoundParameters will contain KV pairs of params already set on the line.
  - Be careful if using data from providers you don't control.
    - API Rate Limits
    - Service outage
- Argument Completers can be defined as ScriptBlocks and referneced with `Register-ArgumentCompleter`
- Can also register with:
  - `[ArgumentCompleter({$varForCompleterBlock.invoke($args)})]`
    - MUST pass `$args` as the input to Invoke
  - `[ArgumentCompleter({Function-Name @args})]`
    - `@args` splatted
- ? Put all ArgumentCompleter scripts in a ArgCompleters.ps1 in /Private
- You can create custom Class Argument Completers:
  - E.x: `[DateRangeCompletions(7,7,'yy.MM.dd')]` 7 days prior and past

  ```powershell
  class DateRangeCompletionsAttribute : ArgumentCompleterAttribute, IArgument

  ```

- Combine with `[ValidateScript]` to ensure value is valid
- If the ArgCompleter returns an object with ` ` or `;` it will cause errors. Wrap in `'` chars to resolve.
- ArgumentCompleter Errors SILENTLY FAIL
  - Use a `try\catch` with a `write-*`
