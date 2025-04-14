# Pimp Your Parameters: The Magic of Transformation Classes

| Room | Time | Speaker |
|------|------|---------|
| 405  | 13:50 - 14:15 | Emrys MacInally |

## Session Description

Ever wished your functions could just "figure it out" when users pass in different types of input? Imagine a world where your function happily accepts either a service name or a service object, and somehow magically knows what to do with either. Welcome to the power of PowerShell transformation classes!
In this session, we'll explore how to make your functions smarter and more flexible without complicating your main code. You'll learn how to create parameters that seamlessly handle multiple input types, automatically converting them to exactly what your function needs. Watch as we transform simple functions into smart ones that "just work," whether users throw service names, objects, or IDs at them.

## Notes

- 2 built-in one for DSC and one for [PSCredential] `[PSCredential][System.Management.Automation.CredentialAttribute()]$cred = 'userName'`
  - Will cast the single string to the UserName of Credential, then cast to PSCred and prompt for Password
  - We've seen this working when passing a UserName to the `-Credential` parameter of functions when that param is defined as type `[PSCredential]`
- Create a custom class that inherrits from TransformationAttribute
- Add `[TransformationAttribureName()]` attribute to Param definition
- Transformation stays with variable. You can re-assign value and it will transform.
- Can itterate arrays
- Transformation Classes can convert and validate data
