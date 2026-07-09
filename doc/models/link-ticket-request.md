
# Link Ticket Request

Link ticket request

*This model accepts additional fields of type object.*

## Structure

`LinkTicketRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeploymentId` | `string` | Required | Deployment ID. Can be found at /deployments, or in your Settings in the web UI. |
| `IssueIds` | `List<string>` | Required | An array of Semgrep finding IDs to link the ticket to. |
| `TicketUrl` | `string` | Required | The URL of the external ticket to link (e.g. https://myorg.atlassian.net/browse/SEC-123). |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

LinkTicketRequest linkTicketRequest = new LinkTicketRequest
{
    DeploymentId = "123",
    IssueIds = new List<string>
    {
        "issue_ids4",
        "issue_ids5",
    },
    TicketUrl = "https://myorg.atlassian.net/browse/SEC-123",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

