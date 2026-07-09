
# Update Project Request

*This model accepts additional fields of type object.*

## Structure

`UpdateProjectRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeploymentSlug` | `string` | Required | Slug of the deployment name. Can be found at `/deployments`, or in your Settings in the web UI. |
| `ManagedScanConfig` | [`ManagedScanConfig`](../../doc/models/managed-scan-config.md) | Optional | [Beta] Configuration of Semgrep Managed Scans for the project, if relevant. |
| `PrimaryBranch` | `string` | Optional | The full name of the branch you would like to set as primary. Use "None" if default_branch is known and you wish to set primary to always be the default branch. |
| `ProjectName` | `string` | Required | Name of the project, typically the repository formatted as a path. |
| `Tags` | `List<string>` | Optional | Tags associated to this project. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

UpdateProjectRequest updateProjectRequest = new UpdateProjectRequest
{
    DeploymentSlug = "your-deployment",
    ProjectName = "organization/project",
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
    PrimaryBranch = "refs/heads/develop",
    Tags = new List<string>
    {
        "tag",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

