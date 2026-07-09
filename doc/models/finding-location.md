
# Finding Location

Location of the record in a file, as reported by Semgrep. If null, then the information does not exist or lacks integrity (older or broken scans)

*This model accepts additional fields of type object.*

## Structure

`FindingLocation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Column` | `long?` | Optional | Column at which the target starts |
| `EndColumn` | `long?` | Optional | Column at which the target ends |
| `EndLine` | `long?` | Optional | Line at which the target ends |
| `FilePath` | `string` | Optional | File path of the relevant line and column numbers |
| `Line` | `long?` | Optional | Line at which the target starts |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

FindingLocation findingLocation = new FindingLocation
{
    Column = 8L,
    EndColumn = 16L,
    EndLine = 124L,
    FilePath = "frontend/src/corpComponents/Code.tsx",
    Line = 120L,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

