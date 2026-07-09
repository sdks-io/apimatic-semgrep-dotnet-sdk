
# Toggle Project Managed Scan Request

*This model accepts additional fields of type object.*

## Structure

`ToggleProjectManagedScanRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeploymentSlug` | `string` | Required | Slug of the deployment name. Can be found at `/deployments`, or in your Settings in the web UI. |
| `DiffScan` | [`ProtosOpenapiV1DiffScan`](../../doc/models/protos-openapi-v1-diff-scan.md) | Optional | - |
| `FullScan` | [`ProtosOpenapiV1FullScan`](../../doc/models/protos-openapi-v1-full-scan.md) | Optional | - |
| `ProjectName` | `string` | Required | Name of the project, typically the repository formatted as a path. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ToggleProjectManagedScanRequest toggleProjectManagedScanRequest = new ToggleProjectManagedScanRequest
{
    DeploymentSlug = "your-deployment",
    ProjectName = "organization/project",
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
};
```

