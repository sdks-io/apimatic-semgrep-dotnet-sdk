
# Protos Sca V1 Sbom Metadata Contact

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1SbomMetadataContact`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Email` | `string` | Optional | - |
| `Name` | `string` | Optional | - |
| `Phone` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosScaV1SbomMetadataContact protosScaV1SbomMetadataContact = new ProtosScaV1SbomMetadataContact
{
    Email = "email0",
    Name = "name6",
    Phone = "phone6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

