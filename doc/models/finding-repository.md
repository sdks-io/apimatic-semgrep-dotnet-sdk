
# Finding Repository

Which repository this finding was identified in

*This model accepts additional fields of type object.*

## Structure

`FindingRepository`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Optional | The repository or named project that the finding is associated with |
| `Url` | `string` | Optional | The source URL from which this repository last scanned |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

FindingRepository findingRepository = new FindingRepository
{
    Name = "semgrep",
    Url = "https://github.com/semgrep/semgrep",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

