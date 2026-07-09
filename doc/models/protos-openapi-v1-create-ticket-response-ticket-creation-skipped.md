
# Protos Openapi V1 Create Ticket Response Ticket Creation Skipped

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IssueIds` | `List<long>` | Optional | List of issue IDs |
| `Reason` | `string` | Optional | The reason why the issue was skipped |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped protosOpenapiV1CreateTicketResponseTicketCreationSkipped = new ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped
{
    IssueIds = new List<long>
    {
        74L,
        75L,
    },
    Reason = "reason4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

