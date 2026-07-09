
# Protos Openapi V1 Get Scan Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1GetScanResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CompletedAt` | `string` | Optional | imestamp of when the scan started. |
| `DeploymentId` | `long?` | Optional | The unique ID of the deployment associated with the scanned repository. |
| `EnabledProducts` | `List<string>` | Optional | The products used when running the scan. |
| `ExitCode` | `long?` | Optional | - |
| `HasLogs` | `bool?` | Optional | - |
| `Id` | `long?` | Optional | The unique ID representing this scan. |
| `Meta` | [`ProtosOpenapiV1GetScanResponseScanMeta`](../../doc/models/protos-openapi-v1-get-scan-response-scan-meta.md) | Optional | - |
| `RepositoryId` | `long?` | Optional | The unique ID of the repository that was scanned. |
| `StartedAt` | `string` | Optional | when the scan was started |
| `Stats` | `object` | Optional | Miscellaneous statistics about the scan, like number of findings found and scan duration. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1GetScanResponse protosOpenapiV1GetScanResponse = new ProtosOpenapiV1GetScanResponse
{
    CompletedAt = "2023-11-18 23:28:12.391807+00:00",
    DeploymentId = 120L,
    EnabledProducts = new List<string>
    {
        "secrets",
    },
    ExitCode = 102L,
    HasLogs = false,
    Id = 123L,
    RepositoryId = 1234567L,
    StartedAt = "2023-11-18 23:28:12.391807+00:00",
    Stats = ApiHelper.JsonDeserialize<object>("{\"findings\":5,\"total_time\":100}"),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

