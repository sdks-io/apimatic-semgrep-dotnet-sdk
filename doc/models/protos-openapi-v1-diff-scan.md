
# Protos Openapi V1 Diff Scan

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1DiffScan`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `bool?` | Optional | When true, diff-aware scans are enabled for the project. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosOpenapiV1DiffScan protosOpenapiV1DiffScan = new ProtosOpenapiV1DiffScan
{
    Enabled = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

