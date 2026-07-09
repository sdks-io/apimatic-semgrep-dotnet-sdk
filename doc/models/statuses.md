
# Statuses

Only get scans that have one of these statuses

| value | description |
|-------|---------------|
| SCAN_STATUS_RUNNING | The scan is currently running |
| SCAN_STATUS_COMPLETED | The scan has completed successfully (0 or 1 exit code) |
| SCAN_STATUS_PENDING | The scan is queued and waiting to start |
| SCAN_STATUS_CANCELLED | The scan was cancelled before completion |
| SCAN_STATUS_ERROR | The scan has exited with a failure (exit code not 0 or 1) |
| SCAN_STATUS_NEVER_FINISHED | The scan did not report an error or success after over an hour |

## Enumeration

`Statuses`

## Fields

| Name |
|  --- |
| `ScanStatusUnspecified` |
| `ScanStatusRunning` |
| `ScanStatusCompleted` |
| `ScanStatusPending` |
| `ScanStatusCancelled` |
| `ScanStatusError` |
| `ScanStatusNeverFinished` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

Statuses statuses = Statuses.ScanStatusCompleted;
```

