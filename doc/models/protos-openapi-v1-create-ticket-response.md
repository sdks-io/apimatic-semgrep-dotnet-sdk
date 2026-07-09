
# Protos Openapi V1 Create Ticket Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1CreateTicketResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Failed` | [`List<ProtosOpenapiV1CreateTicketResponseTicketCreationFailed>`](../../doc/models/protos-openapi-v1-create-ticket-response-ticket-creation-failed.md) | Optional | List of issues where ticket creation failed. This list may include issues that were skipped because they exceed the specified limit. |
| `Skipped` | [`List<ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped>`](../../doc/models/protos-openapi-v1-create-ticket-response-ticket-creation-skipped.md) | Optional | List of issues that were skipped |
| `Succeeded` | [`List<ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess>`](../../doc/models/protos-openapi-v1-create-ticket-response-ticket-creation-success.md) | Optional | List of successfully created tickets |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1CreateTicketResponse protosOpenapiV1CreateTicketResponse = new ProtosOpenapiV1CreateTicketResponse
{
    Failed = new List<ProtosOpenapiV1CreateTicketResponseTicketCreationFailed>
    {
        new ProtosOpenapiV1CreateTicketResponseTicketCreationFailed
        {
            Error = "error6",
            IssueIds = new List<long>
            {
                196L,
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ProtosOpenapiV1CreateTicketResponseTicketCreationFailed
        {
            Error = "error6",
            IssueIds = new List<long>
            {
                196L,
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Skipped = new List<ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped>
    {
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped
        {
            IssueIds = new List<long>
            {
                38L,
            },
            Reason = "reason4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped
        {
            IssueIds = new List<long>
            {
                38L,
            },
            Reason = "reason4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Succeeded = new List<ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess>
    {
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess
        {
            ExternalSlug = "external_slug4",
            IssueIds = new List<long>
            {
                230L,
                229L,
                228L,
            },
            TicketId = 2L,
            TicketUrl = "ticket_url0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess
        {
            ExternalSlug = "external_slug4",
            IssueIds = new List<long>
            {
                230L,
                229L,
                228L,
            },
            TicketId = 2L,
            TicketUrl = "ticket_url0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess
        {
            ExternalSlug = "external_slug4",
            IssueIds = new List<long>
            {
                230L,
                229L,
                228L,
            },
            TicketId = 2L,
            TicketUrl = "ticket_url0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

