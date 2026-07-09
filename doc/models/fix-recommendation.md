
# Fix Recommendation

Recommendation for fixing the vulnerability

*This model accepts additional fields of type object.*

## Structure

`FixRecommendation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Package` | `string` | Optional | The package for which a fix is recommended |
| `Version` | `string` | Optional | The recommended version of the package |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

FixRecommendation fixRecommendation = new FixRecommendation
{
    Package = "System.Drawing.Common",
    Version = "5.0.3",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

