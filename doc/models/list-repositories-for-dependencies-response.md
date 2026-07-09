
# List Repositories for Dependencies Response

*This model accepts additional fields of type object.*

## Structure

`ListRepositoriesForDependenciesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cursor` | `long?` | Optional | Pass to next request to get next page of results. |
| `HasMore` | `bool` | Required | True if there are more repositories to get. |
| `RepositorySummaries` | [`List<ProtosScaV1RepositoryDependencySummary>`](../../doc/models/protos-sca-v1-repository-dependency-summary.md) | Required | List of repositories. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ListRepositoriesForDependenciesResponse listRepositoriesForDependenciesResponse = new ListRepositoriesForDependenciesResponse
{
    HasMore = false,
    RepositorySummaries = new List<ProtosScaV1RepositoryDependencySummary>
    {
        new ProtosScaV1RepositoryDependencySummary
        {
            HasDependencyPathScan = false,
            Id = 140L,
            Name = "name0",
            NumDependencies = 226L,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Cursor = 48L,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

