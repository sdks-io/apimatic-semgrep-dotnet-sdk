
# New Triage State

The triage state you would like to bulk triage your findings to.

## Enumeration

`NewTriageState`

## Fields

| Name |
|  --- |
| `Ignored` |
| `Reviewing` |
| `Fixing` |
| `Reopened` |
| `ProvisionallyIgnored` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

NewTriageState newTriageState = NewTriageState.ProvisionallyIgnored;
```

