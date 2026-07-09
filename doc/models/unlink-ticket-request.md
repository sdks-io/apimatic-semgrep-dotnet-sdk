
# Unlink Ticket Request

Unlink ticket request

*This model accepts additional fields of type object.*

## Structure

`UnlinkTicketRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeploymentId` | `string` | Required | Deployment ID. Can be found at /deployments, or in your Settings in the web UI. |
| `IssueIds` | `List<string>` | Required | An array of Semgrep finding IDs to unlink tickets from. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

UnlinkTicketRequest unlinkTicketRequest = new UnlinkTicketRequest
{
    DeploymentId = "123",
    IssueIds = new List<string>
    {
        "issue_ids2",
        "issue_ids1",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

