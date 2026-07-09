
# List Repositories for Dependencies Request

*This model accepts additional fields of type object.*

## Structure

`ListRepositoriesForDependenciesRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cursor` | `long?` | Optional | Use cursor in response to get next page of results. |
| `DependencyFilter` | [`ProtosScaV1DependencyFilter`](../../doc/models/protos-sca-v1-dependency-filter.md) | Optional | Object to provide dependency details to filter by. |
| `DeploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `PageSize` | `long?` | Optional | Number of repositories per page. Default: 5, min: 1, max: 100.<br><br>**Default**: `5L`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ListRepositoriesForDependenciesRequest listRepositoriesForDependenciesRequest = new ListRepositoriesForDependenciesRequest
{
    DeploymentId = "deploymentId2",
    Cursor = 236L,
    DependencyFilter = new ProtosScaV1DependencyFilter
    {
        Ecosystem = Ecosystem.Mix,
        License = new List<string>
        {
            "license1",
            "license2",
        },
        LicensePolicySettings = LicensePolicySettings.LicensePolicySettingBlock,
        LockfilePath = "lockfilePath6",
        Name = "name2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    PageSize = 100L,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

