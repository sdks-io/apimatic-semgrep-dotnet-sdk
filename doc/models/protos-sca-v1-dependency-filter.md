
# Protos Sca V1 Dependency Filter

Object to provide dependency details to filter by.

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1DependencyFilter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ecosystem` | [`Ecosystem?`](../../doc/models/ecosystem.md) | Optional | Filter by ecosystem (e.g. npm, pypi, etc).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| no_package_manager \|  \|<br>\| npm \|  \|<br>\| pypi \|  \|<br>\| gomod \|  \|<br>\| cargo \|  \|<br>\| maven \|  \|<br>\| gem \|  \|<br>\| composer \|  \|<br>\| nuget \|  \|<br>\| pub \|  \|<br>\| swiftpm \|  \|<br>\| hex \|  \|<br>\| cocoapods \|  \|<br>\| mix \|  \|<br>\| opam \|  \| |
| `License` | `List<string>` | Optional | Filter by license (e.g. MIT). |
| `LicensePolicySettings` | [`LicensePolicySettings?`](../../doc/models/license-policy-settings.md) | Optional | Filter by license policy setting outcome.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| LICENSE_POLICY_SETTING_ALLOW \|  \|<br>\| LICENSE_POLICY_SETTING_COMMENT \|  \|<br>\| LICENSE_POLICY_SETTING_BLOCK \|  \| |
| `LockfilePath` | `string` | Optional | Filter by path to the lockfile (e.g. `foo/bar/package-lock.json`). |
| `Name` | `string` | Optional | Deprecated - use package_filters instead. Filter by dependency name (e.g. lodash). |
| `PackageFilters` | [`List<ProtosScaV1PackageFilter>`](../../doc/models/protos-sca-v1-package-filter.md) | Optional | Multiple package filters with exact name matching and version bounds. |
| `RepositoryId` | `List<long>` | Optional | Repository IDs (numeric) to filter by. Omit if the endpoint has Repository ID as a path parameter.<br>Use Projects endpoints to retrieve Repository IDs. |
| `Transitivity` | [`Transitivity?`](../../doc/models/transitivity.md) | Optional | Filter by transitivity.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| UNKNOWN_TRANSITIVITY \|  \|<br>\| TRANSITIVE \|  \|<br>\| DIRECT \|  \| |
| `Version` | `string` | Optional | Deprecated - use package_filters instead. Filter by dependency version (e.g. 1.0.1). |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosScaV1DependencyFilter protosScaV1DependencyFilter = new ProtosScaV1DependencyFilter
{
    Ecosystem = Ecosystem.Opam,
    License = new List<string>
    {
        "license5",
    },
    LicensePolicySettings = LicensePolicySettings.LicensePolicySettingBlock,
    LockfilePath = "lockfilePath0",
    Name = "name8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

