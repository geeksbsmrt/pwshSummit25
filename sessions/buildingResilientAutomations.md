# Building Resilient Automations with PowerShell

| Room | Time | Speaker |
|------|------|---------|
| 401 | 10:10 - 10:55 | Matthew Dowst |

## Session Description

Dive deep into the art and science of creating resilient, production-grade automations with PowerShell in this 400-level technical session. We'll explore advanced error-handling patterns and practical techniques to build automation scripts that can withstand complex, unpredictable production environments. This talk will focus on the design principles behind idempotent operations, empowering scripts to safely re-run without unintended consequences, and implementing fault-tolerant structures to ensure continuous operation, even under failure conditions.

## Notes

- Don't code for all scenarios
  - Design it in a way to account for most, make it flexible to update as needed.
  - Desing to re-run from point of failure.
- Do I care?
  - If an error occurs, is it a _failure_?
- Never code a `while()` loop without secondary exits.
- When catching errors, it may be easier or more beinficial to catch all errors in a generic `catch{}` without `[typing]` and then `switch()`.
  - This breaks from traditional programming, but is preferred in PowerShell since the error will be wrapped in `PSObject` and may not have correct `[type]`.


- Book: Practical Automation with PowerShell - In book bundle.
- PowerShell weekly newsletter
- PSModules - Get-CommandSplatting
