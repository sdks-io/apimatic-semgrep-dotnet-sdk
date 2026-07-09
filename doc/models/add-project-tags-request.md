
# Add Project Tags Request

*This model accepts additional fields of type object.*

## Structure

`AddProjectTagsRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeploymentSlug` | `string` | Required | Slug of the deployment name. Can be found at `/deployments`, or in your Settings in the web UI. |
| `ProjectName` | `string` | Required | Name of the project, typically the repository formatted as a path. |
| `Tags` | `List<string>` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

AddProjectTagsRequest addProjectTagsRequest = new AddProjectTagsRequest
{
    DeploymentSlug = "your-deployment",
    ProjectName = "organization/project",
    Tags = new List<string>
    {
        "tag",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

