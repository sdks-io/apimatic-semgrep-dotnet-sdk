
# Click to Fix Pr

A pull request created by Semgrep's Click to Fix feature

*This model accepts additional fields of type object.*

## Structure

`ClickToFixPr`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `string` | Optional | When this PR was created |
| `Url` | `string` | Optional | URL of the pull request |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ClickToFixPr clickToFixPr = new ClickToFixPr
{
    CreatedAt = "2024-01-15 10:30:00+00:00",
    Url = "https://github.com/myorg/myrepo/pull/123",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

