
# Protos Openapi V1 Delete Ticket Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1DeleteTicketResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IssueIds` | `List<string>` | Optional | List of issue IDs unlinked from ticket |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1DeleteTicketResponse protosOpenapiV1DeleteTicketResponse = new ProtosOpenapiV1DeleteTicketResponse
{
    IssueIds = new List<string>
    {
        "18759",
        "18760",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

