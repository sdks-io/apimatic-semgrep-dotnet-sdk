
# Protos Ticketing V1 External Ticket

*This model accepts additional fields of type object.*

## Structure

`ProtosTicketingV1ExternalTicket`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalSlug` | `string` | Optional | Identifier of the external ticket (e.g. for Jira, something like OPS-158). |
| `Id` | `string` | Optional | Nango ticket id |
| `LinkedIssueIds` | `List<string>` | Optional | Semgrep issue ids that are linked to this external ticket |
| `Url` | `string` | Optional | URL of the external ticket. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosTicketingV1ExternalTicket protosTicketingV1ExternalTicket = new ProtosTicketingV1ExternalTicket
{
    ExternalSlug = "externalSlug6",
    Id = "id6",
    LinkedIssueIds = new List<string>
    {
        "linkedIssueIds7",
    },
    Url = "url0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

