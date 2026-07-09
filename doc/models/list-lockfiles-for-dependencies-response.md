
# List Lockfiles for Dependencies Response

*This model accepts additional fields of type object.*

## Structure

`ListLockfilesForDependenciesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cursor` | `string` | Optional | Pass to next request to get next page of results. |
| `HasMore` | `bool` | Required | True if there are more lockfiles to get. |
| `LockfileSummaries` | [`List<ProtosScaV1LockfileDependencySummary>`](../../doc/models/protos-sca-v1-lockfile-dependency-summary.md) | Required | List of lockfiles. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ListLockfilesForDependenciesResponse listLockfilesForDependenciesResponse = new ListLockfilesForDependenciesResponse
{
    HasMore = false,
    LockfileSummaries = new List<ProtosScaV1LockfileDependencySummary>
    {
        new ProtosScaV1LockfileDependencySummary
        {
            LockfilePath = "lockfilePath8",
            NumDependencies = 0L,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Cursor = "cursor0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

