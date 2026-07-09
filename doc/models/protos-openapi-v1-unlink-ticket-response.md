
# Protos Openapi V1 Unlink Ticket Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1UnlinkTicketResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `UnlinkedIssueIds` | `List<string>` | Optional | List of finding IDs that were successfully unlinked from their tickets |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1UnlinkTicketResponse protosOpenapiV1UnlinkTicketResponse = new ProtosOpenapiV1UnlinkTicketResponse
{
    UnlinkedIssueIds = new List<string>
    {
        "unlinked_issue_ids6",
        "unlinked_issue_ids7",
        "unlinked_issue_ids8",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

