
# List Project

A project in your organization that uses Semgrep.

*This model accepts additional fields of type object.*

## Structure

`ListProject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `string` | Optional | Time when this project was created. |
| `DefaultBranch` | `string` | Optional | The default branch in the SCM. |
| `Id` | `long` | Required | Unique ID of this project. |
| `LatestScanAt` | `string` | Optional | Time of latest scan, if there is one. |
| `Name` | `string` | Required | Name of the project. |
| `PrimaryBranch` | `string` | Optional | The primary branch of the project, if known. |
| `Tags` | `List<string>` | Required | Tags associated to this project. |
| `Url` | `string` | Optional | URL of the project, if there is one. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ListProject listProject = new ListProject
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
};
```

