
# Protos Sca V1 Repository Dependency Summary

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1RepositoryDependencySummary`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HasDependencyPathScan` | `bool?` | Optional | True if the repository has been scanned with the `hasPathToTransitivityInScans` feature flag<br>which means it will have dependency graph data in DGraph available to query |
| `Id` | `long?` | Optional | ID of repository. |
| `Name` | `string` | Optional | Name of repository. |
| `NumDependencies` | `long?` | Optional | Total number of dependencies in the repository. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosScaV1RepositoryDependencySummary protosScaV1RepositoryDependencySummary = new ProtosScaV1RepositoryDependencySummary
{
    HasDependencyPathScan = false,
    Id = 78L,
    Name = "name4",
    NumDependencies = 164L,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

