# Building a Web App with PowerShell Universal

| Room | Time | Speaker |
|------|------|---------|
| 401  | 9:45 - 10:30 | Adam Driscoll |

## Session Description

In this session, we'll look at building a web app with PowerShell Universal. We'll leverage the PowerShell Universal platform to setup a secure app that onboards users in Azure and provisions resources on their behalf. We'll explore features such as scripts, REST APIs, apps and authentication and authorization. By the end of this session, you'll be able to build your own web app with PowerShell Universal.

## Notes

- PSU in Azure Docker
- Entra ID App Reg
- Graph Modules
- OAuth Grant Flos
  - IDP -> User Login ->
  - Extract Graph Code -> Validate and grant
  - Extract Code and store
- Create and Display Users
- ironmansoftware/universal:latest
  - Hosted Docker image
- `Invoke-UDRedirect` causes a browser redirect event
  - `-OpenInNewWindow`
- He used pre-written code becase "It took me a long time to get this right..."
- `Set-PSUCache -Key -Value $Token -AbsoluteExpiration $TokenExipryTime`
- `New-UDDynamic`
  - Allows access to DOM and waits for loaded event
  - `-LoadingComponent` shows spinner but doesn't stop UI
- `$UAJob` - Contains information about running PSUJob
