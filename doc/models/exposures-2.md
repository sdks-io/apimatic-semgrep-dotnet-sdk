
# Exposures 2

List of exposures or reachability types to filter by. If not specified, returns findings across all exposures. This filter is applicable when `issue_type=sca` is specified. Valid values: reachable, always_reachable, conditionally_reachable, unreachable, unknown

## Enumeration

`Exposures2`

## Fields

| Name |
|  --- |
| `Reachable` |
| `AlwaysReachable` |
| `ConditionallyReachable` |
| `Unreachable` |
| `Unknown` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

Exposures2 exposures2 = Exposures2.Unknown;
```

