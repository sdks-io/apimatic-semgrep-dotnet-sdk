
# Protos Sca V1 Lockfile Dependency Summary

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1LockfileDependencySummary`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LockfilePath` | `string` | Optional | Path to lockfile (e.g. foo/bar/package-lock.json). |
| `NumDependencies` | `long?` | Optional | Total number of dependencies in the lockfile. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosScaV1LockfileDependencySummary protosScaV1LockfileDependencySummary = new ProtosScaV1LockfileDependencySummary
{
    LockfilePath = "lockfilePath6",
    NumDependencies = 152L,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

