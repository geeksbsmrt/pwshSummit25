# MSAL Authentication: Auth isn't hard (Auth isn't easy either)

| Room | Time | Speaker |
|------|------|---------|
| 404 | 1:00 - 1:45 | Ben Reader |

## Session Description

It's 2025, and somehow, authentication is still a barrier to entry for many IT Pros looking to build tooling and automation for their workloads. Let's dive in and demystify the MSAL authentication world and learn how to leverage it in your PowerShell scripts to authenticate against Microsoft Graph, Azure, and more.

## Notes

- MSAL in PwSh is rough.
  - It has some extraction\extrapolation issues.
  - Known issue: Loading 2 different versions of the same library will silently fail.
    - MS Graph and AZModules use different versions of MSAL and cause issues.
