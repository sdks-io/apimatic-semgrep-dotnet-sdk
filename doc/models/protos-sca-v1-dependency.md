
# Protos Sca V1 Dependency

A specific dependency.

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1Dependency`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Optional | String identifier of dependency |
| `VersionSpecifier` | `string` | Optional | Version specifier of dependency. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosScaV1Dependency protosScaV1Dependency = new ProtosScaV1Dependency
{
    Name = "name2",
    VersionSpecifier = "versionSpecifier0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

