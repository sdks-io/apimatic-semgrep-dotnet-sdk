
# Cyclonedx Version

CycloneDX schema version for the SBOM export. Supported: 1.4, 1.5, 1.6, 1.7. Defaults to 1.4 when unset.

| value | description |
|-------|---------------|
| SBOM_CYCLONE_DX_VERSION_V1_4 |  |
| SBOM_CYCLONE_DX_VERSION_V1_5 |  |
| SBOM_CYCLONE_DX_VERSION_V1_6 |  |
| SBOM_CYCLONE_DX_VERSION_V1_7 |  |

## Enumeration

`CyclonedxVersion`

## Fields

| Name |
|  --- |
| `SbomCycloneDxVersionV14` |
| `SbomCycloneDxVersionV15` |
| `SbomCycloneDxVersionV16` |
| `SbomCycloneDxVersionV17` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

CyclonedxVersion cyclonedxVersion = CyclonedxVersion.SbomCycloneDxVersionV14;
```

