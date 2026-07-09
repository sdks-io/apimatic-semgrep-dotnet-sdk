
# Protos Openapi V1 Create Ticket Response Ticket Creation Success

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalSlug` | `string` | Optional | The external slug identifier for the ticket |
| `IssueIds` | `List<long>` | Optional | List of issue IDs |
| `TicketId` | `long?` | Optional | The ID of the created ticket |
| `TicketUrl` | `string` | Optional | The URL of the created ticket |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess protosOpenapiV1CreateTicketResponseTicketCreationSuccess = new ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess
{
    ExternalSlug = "external_slug8",
    IssueIds = new List<long>
    {
        118L,
        117L,
    },
    TicketId = 114L,
    TicketUrl = "ticket_url6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

