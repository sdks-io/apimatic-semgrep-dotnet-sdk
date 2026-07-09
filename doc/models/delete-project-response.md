
# Delete Project Response

Successfully deleted the project.

*This model accepts additional fields of type object.*

## Structure

`DeleteProjectResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ProjectName` | `string` | Required | The name of the deleted project. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

DeleteProjectResponse deleteProjectResponse = new DeleteProjectResponse
{
    ProjectName = "organization/project",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

