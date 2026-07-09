
# List Dependencies Request

*This model accepts additional fields of type object.*

## Structure

`ListDependenciesRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cursor` | `string` | Optional | Cursor to paginate through the dependencies. Provide a cursor value from the response to retrieve the next page. |
| `DependencyFilter` | [`ProtosScaV1DependencyFilter`](../../doc/models/protos-sca-v1-dependency-filter.md) | Optional | Object to provide dependency details to filter by. |
| `DeploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `PageSize` | `long?` | Optional | Number of dependencies per page. Default: 1000, min: 1, max: 10000.<br><br>**Constraints**: `>= 1`, `<= 10000` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ListDependenciesRequest listDependenciesRequest = new ListDependenciesRequest
{
    DeploymentId = "123",
    Cursor = "cursor2",
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
    PageSize = 1000L,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

