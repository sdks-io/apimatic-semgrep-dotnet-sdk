
# Protos Sca V1 Found Dependency

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1FoundDependency`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DefinedAt` | [`ProtosScaV1CodeLocation`](../../doc/models/protos-sca-v1-code-location.md) | Optional | Path and line number dependency is declared in. |
| `Ecosystem` | [`Ecosystem1?`](../../doc/models/ecosystem-1.md) | Optional | The ecosystem the dependency is in (e.g. pypi, npm, etc).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| no_package_manager \|  \|<br>\| npm \|  \|<br>\| pypi \|  \|<br>\| gomod \|  \|<br>\| cargo \|  \|<br>\| maven \|  \|<br>\| gem \|  \|<br>\| composer \|  \|<br>\| nuget \|  \|<br>\| pub \|  \|<br>\| swiftpm \|  \|<br>\| hex \|  \|<br>\| cocoapods \|  \|<br>\| mix \|  \|<br>\| opam \|  \| |
| `Licenses` | `List<string>` | Optional | Licenses the dependency is using. |
| `ManifestDefinition` | [`ProtosScaV1CodeLocation`](../../doc/models/protos-sca-v1-code-location.md) | Optional | Path to the manifest file that defines the subproject containing this dependency |
| `Package` | [`ProtosScaV1Dependency`](../../doc/models/protos-sca-v1-dependency.md) | Optional | What the dependency is. |
| `RepositoryId` | `string` | Optional | ID of repository dependency is found in. |
| `ResolvedUrl` | `string` | Optional | The resolved URL of the dependency. Could point to a compressed source code directory (e.g. tarball), source code repository, or a package manager cache directory. May be empty if the package manager doesn't supply a URL. |
| `Transitivity` | [`Transitivity1?`](../../doc/models/transitivity-1.md) | Optional | Whether dependency is direct or transitive.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| UNKNOWN_TRANSITIVITY \|  \|<br>\| TRANSITIVE \|  \|<br>\| DIRECT \|  \| |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

ProtosScaV1FoundDependency protosScaV1FoundDependency = new ProtosScaV1FoundDependency
{
    DefinedAt = new ProtosScaV1CodeLocation
    {
        CommittedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        EndCol = "endCol8",
        EndLine = "endLine2",
        Path = "path2",
        StartCol = "startCol2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Ecosystem = Ecosystem1.Gem,
    Licenses = new List<string>
    {
        "licenses5",
        "licenses6",
        "licenses7",
    },
    ManifestDefinition = new ProtosScaV1CodeLocation
    {
        CommittedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        EndCol = "endCol0",
        EndLine = "endLine4",
        Path = "path4",
        StartCol = "startCol4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Package = new ProtosScaV1Dependency
    {
        Name = "name8",
        VersionSpecifier = "versionSpecifier6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

