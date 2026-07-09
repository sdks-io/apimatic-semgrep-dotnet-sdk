
# Protos Scan V1 Scan Public

*This model accepts additional fields of type object.*

## Structure

`ProtosScanV1ScanPublic`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Branch` | `string` | Optional | The scanned branch |
| `Commit` | `string` | Optional | The commit hash that was scanned |
| `CompletedAt` | `DateTime?` | Optional | The timestamp when this scan completed (if it has completed). |
| `DeploymentId` | `string` | Optional | Unique identifier for the deployment of the scan. |
| `EnabledProducts` | `List<string>` | Optional | The products used when running the scan. |
| `ExitCode` | `string` | Optional | The exit_code of the scan (see https://semgrep.dev/docs/cli-reference#exit-codes) |
| `FindingsCounts` | [`ProtosScanV1ScanFindingsCounts`](../../doc/models/protos-scan-v1-scan-findings-counts.md) | Optional | - |
| `Id` | `string` | Optional | ID of the scan. |
| `IsFullScan` | `bool?` | Optional | Whether the scan was a full scan (true) or a diff scan (false) |
| `RepositoryId` | `string` | Optional | Unique identifier for the repository of the scan. |
| `StartedAt` | `DateTime?` | Optional | The timestamp when this scan started. |
| `Status` | [`Status7?`](../../doc/models/status-7.md) | Optional | The current status of the scan<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SCAN_STATUS_RUNNING \| The scan is currently running \|<br>\| SCAN_STATUS_COMPLETED \| The scan has completed successfully (0 or 1 exit code) \|<br>\| SCAN_STATUS_PENDING \| The scan is queued and waiting to start \|<br>\| SCAN_STATUS_CANCELLED \| The scan was cancelled before completion \|<br>\| SCAN_STATUS_ERROR \| The scan has exited with a failure (exit code not 0 or 1) \|<br>\| SCAN_STATUS_NEVER_FINISHED \| The scan did not report an error or success after over an hour \| |
| `TotalTime` | `double?` | Optional | Duration of scan, in seconds |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

ProtosScanV1ScanPublic protosScanV1ScanPublic = new ProtosScanV1ScanPublic
{
    Branch = "main",
    Commit = "6d3de02545f820febf2af9820568fa5f697d4087",
    CompletedAt = DateTime.ParseExact("2020-11-18 23:30:10.216670+00:00", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    DeploymentId = "deployment_id0",
    EnabledProducts = new List<string>
    {
        "secrets",
    },
    ExitCode = "0",
    IsFullScan = true,
    StartedAt = DateTime.ParseExact("2020-11-18 23:28:12.391807+00:00", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Status = Status7.ScanStatusRunning,
    TotalTime = 17.32,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

