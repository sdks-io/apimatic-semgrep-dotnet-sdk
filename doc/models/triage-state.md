
# Triage State

The finding's triage state. Note: "reviewing" and "fixing" are only in private beta. Set by the user and used along with state to generate the final "status" viewable in the UI

## Enumeration

`TriageState`

## Fields

| Name |
|  --- |
| `Untriaged` |
| `Ignored` |
| `Reopened` |
| `Reviewing` |
| `Fixing` |
| `ProvisionallyIgnored` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

TriageState triageState = TriageState.Untriaged;
```

