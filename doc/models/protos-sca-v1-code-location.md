
# Protos Sca V1 Code Location

Specific location in a file.

*This model accepts additional fields of type object.*

## Structure

`ProtosScaV1CodeLocation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CommittedAt` | `DateTime?` | Optional | Timestamp when code file was last modified, if available. |
| `EndCol` | `string` | Optional | Ending column number (1 indexed). |
| `EndLine` | `string` | Optional | Ending line number (1 indexed). |
| `Path` | `string` | Optional | Path to a file. |
| `StartCol` | `string` | Optional | Starting column number (1 indexed). |
| `StartLine` | `string` | Optional | Starting line number (1 indexed). |
| `Url` | `string` | Optional | URL to code location if available, otherwise empty. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Globalization;

ProtosScaV1CodeLocation protosScaV1CodeLocation = new ProtosScaV1CodeLocation
{
    CommittedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    EndCol = "endCol6",
    EndLine = "endLine0",
    Path = "path0",
    StartCol = "startCol0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

