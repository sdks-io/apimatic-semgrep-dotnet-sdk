
# Protos Openapi V1 Full Scan

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1FullScan`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `bool?` | Optional | When true, weekly full scans are enabled. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosOpenapiV1FullScan protosOpenapiV1FullScan = new ProtosOpenapiV1FullScan
{
    Enabled = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

