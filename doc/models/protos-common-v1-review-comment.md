
# Protos Common V1 Review Comment

*This model accepts additional fields of type object.*

## Structure

`ProtosCommonV1ReviewComment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalDiscussionId` | `string` | Optional | External ID of the review comment or discussion thread. |
| `ExternalNoteId` | `string` | Optional | External ID of the specific note in the review comment discussion thread. Only applicable for GitLab.com, GitLab Self-Managed and Azure DevOps. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosCommonV1ReviewComment protosCommonV1ReviewComment = new ProtosCommonV1ReviewComment
{
    ExternalDiscussionId = "externalDiscussionId8",
    ExternalNoteId = "externalNoteId0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

