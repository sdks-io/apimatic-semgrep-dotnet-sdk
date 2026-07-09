
# Found Dependency

Information about the vulnerable package that was found in the codebase

*This model accepts additional fields of type object.*

## Structure

`FoundDependency`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ecosystem` | [`Ecosystem2?`](../../doc/models/ecosystem-2.md) | Optional | Ecosystem of the package<br><br>**Default**: `Ecosystem2.no_package_manager` |
| `LockfileLineUrl` | `string` | Optional | URL to the specific line in the lockfile where the dependency is listed |
| `Package` | `string` | Optional | Name of the package that contains the vulnerability |
| `Transitivity` | [`Transitivity2?`](../../doc/models/transitivity-2.md) | Optional | Indicates whether the dependency is direct or transitive |
| `Version` | `string` | Optional | Version of the package that was found to be vulnerable |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

FoundDependency foundDependency = new FoundDependency
{
    Ecosystem = Ecosystem2.Npm,
    LockfileLineUrl = "https://github.com/yourorg/yourrepo/blob/main/package-lock.json#L25",
    Package = "System.Drawing.Common",
    Transitivity = Transitivity2.Direct,
    Version = "5.0.0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

