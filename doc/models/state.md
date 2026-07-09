
# State

The finding's resolution state. Managed only by changes detected at scan time, the `state` is combined with `triage_state` to ultimately determine a final `status` which is exposed in the UI and API

## Enumeration

`State`

## Fields

| Name |
|  --- |
| `Fixed` |
| `Muted` |
| `Unresolved` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

State state = State.Unresolved;
```

