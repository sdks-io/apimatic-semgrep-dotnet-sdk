
# Create Sbom Export Response

*This model accepts additional fields of type object.*

## Structure

`CreateSbomExportResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `TaskToken` | `string` | Required | Task token for the SBOM export job. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

CreateSbomExportResponse createSbomExportResponse = new CreateSbomExportResponse
{
    TaskToken = "taskToken6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

