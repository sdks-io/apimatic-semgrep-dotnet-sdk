
# Protos Ai V1 Autotriage

*This model accepts additional fields of type object.*

## Structure

`ProtosAiV1Autotriage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Feedback` | [`ProtosAiV1AutotriageFeedback`](../../doc/models/protos-ai-v1-autotriage-feedback.md) | Optional | - |
| `Id` | `string` | Optional | - |
| `IssueId` | `string` | Optional | - |
| `MatchBasedId` | `string` | Optional | - |
| `MemoryIdsReferenced` | `List<string>` | Optional | - |
| `MemoryIdsRendered` | `List<string>` | Optional | - |
| `Reason` | `string` | Optional | The reasoning for a false positive verdict, explaining why you might want to ignore the finding. Empty string if verdict is true positive. |
| `Verdict` | [`Verdict?`](../../doc/models/verdict.md) | Optional | \| value \| description \|<br>\|-------\|---------------\|<br>\| VERDICT_TRUE_POSITIVE \|  \|<br>\| VERDICT_FALSE_POSITIVE \|  \|<br>\| VERDICT_NO_VERDICT \|  \| |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosAiV1Autotriage protosAiV1Autotriage = new ProtosAiV1Autotriage
{
    Feedback = new ProtosAiV1AutotriageFeedback
    {
        AutotriageId = "autotriageId0",
        Note = "note2",
        Rating = Rating.RatingGood,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Id = "id0",
    IssueId = "issueId8",
    MatchBasedId = "matchBasedId2",
    MemoryIdsReferenced = new List<string>
    {
        "memoryIdsReferenced2",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

