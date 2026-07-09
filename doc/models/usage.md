
# Usage

Usage of the vulnerable package in the codebase. Applies to reachable findings

*This model accepts additional fields of type object.*

## Structure

`Usage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalTicket` | [`ExternalTicket`](../../doc/models/external-ticket.md) | Optional | External ticket associated with finding |
| `Location` | [`FindingLocation`](../../doc/models/finding-location.md) | Optional | Location of the record in a file, as reported by Semgrep. If null, then the information does not exist or lacks integrity (older or broken scans) |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

Usage usage = new Usage
{
    ExternalTicket = new ExternalTicket
    {
        ExternalSlug = "external_slug4",
        Id = 228L,
        LinkedIssueIds = new List<long>
        {
            115L,
            116L,
            117L,
        },
        Url = "url8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Location = new FindingLocation
    {
        Column = 222L,
        EndColumn = 174L,
        EndLine = 120L,
        FilePath = "file_path0",
        Line = 114L,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

