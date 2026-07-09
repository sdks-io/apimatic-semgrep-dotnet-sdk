
# Protos Sca V1 Package Filter

Individual package filter with optional version bounds.

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1PackageFilter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExactNameMatch` | `bool?` | Optional | When true, name must match exactly. When false (default), name is fuzzy-matched (contains). |
| `ExactVersion` | `string` | Optional | Exact version match (e.g. "1.0.0").<br>Takes precedence over version bounds if set. |
| `Name` | `string` | Optional | Exact package name (e.g. lodash). |
| `VersionLowerBound` | `string` | Optional | Lower bound version constraint (e.g. ">=1.0.0").<br>Ignored if exact_version is set. |
| `VersionUpperBound` | `string` | Optional | Upper bound version constraint (e.g. "<2.0.0").<br>Ignored if exact_version is set. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosScaV1PackageFilter protosScaV1PackageFilter = new ProtosScaV1PackageFilter
{
    ExactNameMatch = false,
    ExactVersion = "exactVersion4",
    Name = "name6",
    VersionLowerBound = "versionLowerBound8",
    VersionUpperBound = "versionUpperBound8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

