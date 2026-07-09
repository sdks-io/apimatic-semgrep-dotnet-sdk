
# Validation State 2

Whether the finding was validated or not.

| value | description |
|-------|---------------|
| VALIDATION_STATE_CONFIRMED_VALID |  |
| VALIDATION_STATE_CONFIRMED_INVALID |  |
| VALIDATION_STATE_VALIDATION_ERROR |  |
| VALIDATION_STATE_NO_VALIDATOR |  |

## Enumeration

`ValidationState2`

## Fields

| Name |
|  --- |
| `ValidationStateConfirmedValid` |
| `ValidationStateConfirmedInvalid` |
| `ValidationStateValidationError` |
| `ValidationStateNoValidator` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

ValidationState2 validationState2 = ValidationState2.ValidationStateValidationError;
```

