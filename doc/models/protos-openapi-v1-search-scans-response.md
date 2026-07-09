
# Protos Openapi V1 Search Scans Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1SearchScansResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cursor` | `string` | Optional | Cursor to retrieve the next page of results. |
| `Scans` | [`List<ProtosScanV1ScanPublic>`](../../doc/models/protos-scan-v1-scan-public.md) | Optional | List of scans. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

ProtosOpenapiV1SearchScansResponse protosOpenapiV1SearchScansResponse = new ProtosOpenapiV1SearchScansResponse
{
    Cursor = "cursor8",
    Scans = new List<ProtosScanV1ScanPublic>
    {
        new ProtosScanV1ScanPublic
        {
            Branch = "branch6",
            Commit = "commit2",
            CompletedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            DeploymentId = "deployment_id4",
            EnabledProducts = new List<string>
            {
                "enabled_products6",
                "enabled_products7",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ProtosScanV1ScanPublic
        {
            Branch = "branch6",
            Commit = "commit2",
            CompletedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            DeploymentId = "deployment_id4",
            EnabledProducts = new List<string>
            {
                "enabled_products6",
                "enabled_products7",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

