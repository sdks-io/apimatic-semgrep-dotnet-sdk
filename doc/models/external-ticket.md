
# External Ticket

External ticket associated with finding

*This model accepts additional fields of type object.*

## Structure

`ExternalTicket`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalSlug` | `string` | Optional | Identifier of the external ticket |
| `Id` | `long?` | Optional | External ticket id |
| `LinkedIssueIds` | `List<long>` | Optional | Semgrep issue ids that are linked to this external ticket |
| `Url` | `string` | Optional | URL of the external ticket |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ExternalTicket externalTicket = new ExternalTicket
{
    ExternalSlug = "OPS-158",
    Id = 74L,
    LinkedIssueIds = new List<long>
    {
        217L,
        218L,
    },
    Url = "url0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

