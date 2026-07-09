
# Protos Openapi V1 Create Ticket Response Ticket Creation Failed

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1CreateTicketResponseTicketCreationFailed`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | `string` | Optional | The error message for the failure |
| `IssueIds` | `List<long>` | Optional | List of issue IDs |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1CreateTicketResponseTicketCreationFailed protosOpenapiV1CreateTicketResponseTicketCreationFailed = new ProtosOpenapiV1CreateTicketResponseTicketCreationFailed
{
    Error = "error8",
    IssueIds = new List<long>
    {
        36L,
        37L,
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

