
# Float Range

*This model accepts additional fields of type object.*

## Structure

`FloatRange`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Max` | `double?` | Optional | End of the range |
| `Min` | `double?` | Optional | Start of the range |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

FloatRange floatRange = new FloatRange
{
    Max = 69.02,
    Min = 4.4,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

