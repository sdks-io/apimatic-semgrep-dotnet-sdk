
# Update Project Response

Successfully updated details for the project.

*This model accepts additional fields of type object.*

## Structure

`UpdateProjectResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Project` | [`Project`](../../doc/models/project.md) | Required | A project in your organization that uses Semgrep. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

UpdateProjectResponse updateProjectResponse = new UpdateProjectResponse
{
    Project = new Project
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
        ManagedScanConfig = new ManagedScanConfig
        {
            DiffScan = new ProtosOpenapiV1DiffScan
            {
                Enabled = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            FullScan = new ProtosOpenapiV1FullScan
            {
                Enabled = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        PrimaryBranch = "refs/heads/custom-main",
        Url = "https://github.com/returntocorp/semgrep",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

