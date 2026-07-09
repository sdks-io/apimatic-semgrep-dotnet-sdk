
# List Projects Response

Return the list of projects in an organization.

*This model accepts additional fields of type object.*

## Structure

`ListProjectsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Projects` | [`List<ListProject>`](../../doc/models/list-project.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ListProjectsResponse listProjectsResponse = new ListProjectsResponse
{
    Projects = new List<ListProject>
    {
        new ListProject
        {
            Id = 1234567L,
            Name = "returntocorp/semgrep",
            Tags = new List<string>
            {
                "tag",
            },
            CreatedAt = "2020-11-18 23:28:12.391807+00:00",
            DefaultBranch = "refs/heads/main",
            LatestScanAt = "2023-01-13 20:51:51.449081+00:00",
            PrimaryBranch = "refs/heads/custom-main",
            Url = "https://github.com/returntocorp/semgrep",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

