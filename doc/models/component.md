
# Component

Semgrep Assistant's guess as for what the matched source code's purpose is

*This model accepts additional fields of type object.*

## Structure

`Component`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Risk` | [`Risk?`](../../doc/models/risk.md) | Optional | Component risk level |
| `Tag` | `string` | Optional | Component tag |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

Component component = new Component
{
    Risk = Risk.High,
    Tag = "user data",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

