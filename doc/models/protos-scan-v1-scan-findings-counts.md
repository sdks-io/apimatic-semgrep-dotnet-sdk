
# Protos Scan V1 Scan Findings Counts

*This model accepts additional fields of type object.*

## Structure

`ProtosScanV1ScanFindingsCounts`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Code` | `string` | Optional | Total number of Code findings in the scan |
| `Secrets` | `string` | Optional | Total number of Secrets findings in the scan |
| `SupplyChain` | `string` | Optional | Total number of Supply Chain findings in the scan |
| `Total` | `string` | Optional | Total number of findings in the scan |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosScanV1ScanFindingsCounts protosScanV1ScanFindingsCounts = new ProtosScanV1ScanFindingsCounts
{
    Code = "2",
    Secrets = "1",
    SupplyChain = "1",
    Total = "4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

