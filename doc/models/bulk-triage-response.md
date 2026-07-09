
# Bulk Triage Response

*This model accepts additional fields of type object.*

## Structure

`BulkTriageResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NumTriaged` | `long` | Required | Number of items updated |
| `TriagedIssues` | `List<long>` | Required | List of triaged issue IDs |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

BulkTriageResponse bulkTriageResponse = new BulkTriageResponse
{
    NumTriaged = 232L,
    TriagedIssues = new List<long>
    {
        68L,
        69L,
        70L,
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

