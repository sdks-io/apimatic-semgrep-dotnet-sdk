
# Exposures

Filter by exposure (reachability type). Only applies for sca findings. Reachability is the ability of an attacker to access a vulnerability in a system.

## Enumeration

`Exposures`

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

Exposures exposures = Exposures.AlwaysReachable;
```

