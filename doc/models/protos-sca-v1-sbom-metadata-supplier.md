
# Protos Sca V1 Sbom Metadata Supplier

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1SbomMetadataSupplier`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Contact` | [`ProtosScaV1SbomMetadataContact`](../../doc/models/protos-sca-v1-sbom-metadata-contact.md) | Optional | - |
| `Name` | `string` | Optional | - |
| `Url` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosScaV1SbomMetadataSupplier protosScaV1SbomMetadataSupplier = new ProtosScaV1SbomMetadataSupplier
{
    Contact = new ProtosScaV1SbomMetadataContact
    {
        Email = "email4",
        Name = "name2",
        Phone = "phone2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Name = "name2",
    Url = "url6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

