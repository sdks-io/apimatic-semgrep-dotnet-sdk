
# Protos Openapi V1 Link Ticket Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1LinkTicketResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalSlug` | `string` | Optional | The external slug identifier for the ticket (e.g. SEC-123) |
| `LinkedIssueIds` | `List<string>` | Optional | List of finding IDs that were successfully linked to the ticket |
| `ReplacedIssueIds` | `List<string>` | Optional | List of finding IDs where an existing ticket link was replaced |
| `TicketId` | `long?` | Optional | The internal ID of the linked ticket record |
| `TicketUrl` | `string` | Optional | The URL of the linked ticket |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1LinkTicketResponse protosOpenapiV1LinkTicketResponse = new ProtosOpenapiV1LinkTicketResponse
{
    ExternalSlug = "external_slug4",
    LinkedIssueIds = new List<string>
    {
        "linked_issue_ids1",
    },
    ReplacedIssueIds = new List<string>
    {
        "replaced_issue_ids5",
    },
    TicketId = 148L,
    TicketUrl = "ticket_url8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

