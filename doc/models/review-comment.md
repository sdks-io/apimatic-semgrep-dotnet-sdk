
# Review Comment

External review comment information associated with a finding

*This model accepts additional fields of type object.*

## Structure

`ReviewComment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalDiscussionId` | `string` | Optional | External ID of the review comment or discussion thread |
| `ExternalNoteId` | `string` | Optional | External ID of the specific note in the review comment discussion thread. Only applicable for GitLab.com, GitLab Self-Managed and Azure DevOps |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ReviewComment reviewComment = new ReviewComment
{
    ExternalDiscussionId = "af04762b69acfb74c8f9",
    ExternalNoteId = "123523",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

