
# Protos Ai V1 Autotriage Feedback

*This model accepts additional fields of type object.*

## Structure

`ProtosAiV1AutotriageFeedback`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutotriageId` | `string` | Optional | - |
| `Note` | `string` | Optional | - |
| `Rating` | [`Rating?`](../../doc/models/rating.md) | Optional | \| value \| description \|<br>\|-------\|---------------\|<br>\| RATING_GOOD \| Autotriage rated positively by a user. \|<br>\| RATING_BAD \| Autotriage rated negatively by a user. \| |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosAiV1AutotriageFeedback protosAiV1AutotriageFeedback = new ProtosAiV1AutotriageFeedback
{
    AutotriageId = "autotriageId4",
    Note = "note4",
    Rating = Rating.RatingGood,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

