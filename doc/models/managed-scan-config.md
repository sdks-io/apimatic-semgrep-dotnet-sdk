
# Managed Scan Config

[Beta] Configuration of Semgrep Managed Scans for the project, if relevant.

*This model accepts additional fields of type object.*

## Structure

`ManagedScanConfig`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DiffScan` | [`ProtosOpenapiV1DiffScan`](../../doc/models/protos-openapi-v1-diff-scan.md) | Optional | - |
| `FullScan` | [`ProtosOpenapiV1FullScan`](../../doc/models/protos-openapi-v1-full-scan.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ManagedScanConfig managedScanConfig = new ManagedScanConfig
{
    DiffScan = new ProtosOpenapiV1DiffScan
    {
        Enabled = false,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    FullScan = new ProtosOpenapiV1FullScan
    {
        Enabled = false,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

