
# Protos Sca V1 Sbom Format Version

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1SbomFormatVersion`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CyclonedxVersion` | [`CyclonedxVersion?`](../../doc/models/cyclonedx-version.md) | Optional | CycloneDX schema version for the SBOM export. Supported: 1.4, 1.5, 1.6, 1.7. Defaults to 1.4 when unset.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_CYCLONE_DX_VERSION_V1_4 \|  \|<br>\| SBOM_CYCLONE_DX_VERSION_V1_5 \|  \|<br>\| SBOM_CYCLONE_DX_VERSION_V1_6 \|  \|<br>\| SBOM_CYCLONE_DX_VERSION_V1_7 \|  \| |
| `Format` | [`Format?`](../../doc/models/format.md) | Optional | Format for the SBOM export.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_FORMAT_CYCLONEDX \|  \|<br><br>**Default**: `Format.SBOM_FORMAT_CYCLONEDX` |
| `Version` | `string` | Optional | Deprecated. Use `cyclonedx_version`. Free-text CycloneDX version, e.g. "1.7". |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosScaV1SbomFormatVersion protosScaV1SbomFormatVersion = new ProtosScaV1SbomFormatVersion
{
    CyclonedxVersion = CyclonedxVersion.SbomCycloneDxVersionV16,
    Format = Format.SbomFormatCyclonedx,
    Version = "version6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

