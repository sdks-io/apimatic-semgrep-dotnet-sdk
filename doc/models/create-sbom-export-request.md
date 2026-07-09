
# Create Sbom Export Request

*This model accepts additional fields of type object.*

## Structure

`CreateSbomExportRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `FormatVersion` | [`ProtosScaV1SbomFormatVersion`](../../doc/models/protos-sca-v1-sbom-format-version.md) | Optional | - |
| `MetadataComponentType` | [`MetadataComponentType?`](../../doc/models/metadata-component-type.md) | Optional | Metadata component type for the SBOM export.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_APPLICATION \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_FRAMEWORK \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_LIBRARY \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_CONTAINER \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_PLATFORM \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_OPERATING_SYSTEM \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_DEVICE \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_DEVICE_DRIVER \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_FIRMWARE \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_FILE \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_MACHINE_LEARNING_MODEL \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_DATA \|  \|<br><br>**Default**: `MetadataComponentType.SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_APPLICATION` |
| `MetadataSupplier` | [`ProtosScaV1SbomMetadataSupplier`](../../doc/models/protos-sca-v1-sbom-metadata-supplier.md) | Optional | - |
| `Ref` | `string` | Optional | Branch to export SBOM for (Ex. ref=`refs/pull/1234/merge`). |
| `RepositoryId` | `string` | Optional | Repository ID to export SBOM for. |
| `SbomOutputFormat` | [`SbomOutputFormat?`](../../doc/models/sbom-output-format.md) | Optional | SBOM output format for the SBOM export.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_OUTPUT_FORMAT_JSON \|  \| |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

CreateSbomExportRequest createSbomExportRequest = new CreateSbomExportRequest
{
    DeploymentId = "123",
    FormatVersion = new ProtosScaV1SbomFormatVersion
    {
        CyclonedxVersion = CyclonedxVersion.SbomCycloneDxVersionV16,
        Format = Format.SbomFormatCyclonedx,
        Version = "version8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    MetadataComponentType = MetadataComponentType.SbomMetadataComponentTypeCycloneDxV15Application,
    MetadataSupplier = new ProtosScaV1SbomMetadataSupplier
    {
        Contact = new ProtosScaV1SbomMetadataContact
        {
            Email = "email4",
            Name = "name2",
            Phone = "phone2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Name = "name4",
        Url = "url8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    MRef = "refs/pull/1234/merge",
    RepositoryId = "123",
    SbomOutputFormat = SbomOutputFormat.SbomOutputFormatJson,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

