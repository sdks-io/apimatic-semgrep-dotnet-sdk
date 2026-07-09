
# Validation State

Filter by whether a secret could be validated. Only applies for secrets findings.

## Enumeration

`ValidationState`

## Fields

| Name |
|  --- |
| `ConfirmedValid` |
| `ConfirmedInvalid` |
| `ValidationError` |
| `NoValidator` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

ValidationState validationState = ValidationState.ValidationError;
```

