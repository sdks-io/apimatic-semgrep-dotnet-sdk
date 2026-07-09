
# Status 8

Status of the finding.

- FINDING_STATUS_UNSPECIFIED: Return results for all finding statuses (if used as a parameter).
- FINDING_STATUS_OPEN: Finding is open and needs to be triaged
- FINDING_STATUS_IGNORED: Finding has been triaged and is being ignored
- FINDING_STATUS_FIXED: Finding has been fixed
- FINDING_STATUS_REMOVED: Finding has been removed
- FINDING_STATUS_UNKNOWN: Finding status is unknown

## Enumeration

`Status8`

## Fields

| Name |
|  --- |
| `FindingStatusUnspecified` |
| `FindingStatusOpen` |
| `FindingStatusIgnored` |
| `FindingStatusFixed` |
| `FindingStatusRemoved` |
| `FindingStatusUnknown` |
| `FindingStatusProvisionallyIgnored` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

Status8 status8 = Status8.FindingStatusIgnored;
```

