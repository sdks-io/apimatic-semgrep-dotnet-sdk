
# Protos Secrets V1 Secrets Finding

A Finding represents a single secret finding.

*This model accepts additional fields of type object.*

## Structure

`ProtosSecretsV1SecretsFinding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Autotriage` | [`ProtosAiV1Autotriage`](../../doc/models/protos-ai-v1-autotriage.md) | Optional | * Autotriage info for the finding.<br>  This is used for the Generic Secrets Detection project, for<br>  autotriaging secrets findings with LLMs |
| `Confidence` | [`Confidence7?`](../../doc/models/confidence-7.md) | Optional | Confidence of the finding.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| CONFIDENCE_HIGH \|  \|<br>\| CONFIDENCE_MEDIUM \|  \|<br>\| CONFIDENCE_LOW \|  \| |
| `CreatedAt` | `DateTime?` | Optional | Creation timestamp. |
| `ExternalTicket` | [`ProtosTicketingV1ExternalTicket`](../../doc/models/protos-ticketing-v1-external-ticket.md) | Optional | The external ticket reference |
| `FindingPath` | `string` | Optional | File path where the finding was detected. |
| `FindingPathUrl` | `string` | Optional | URL to the file where the finding was detected. |
| `HistoricalInfo` | [`ProtosSecretsV1HistoricalInfo`](../../doc/models/protos-secrets-v1-historical-info.md) | Optional | Historical scanning info for the finding. |
| `Id` | `string` | Optional | ID of the finding. |
| `Mode` | [`Mode?`](../../doc/models/mode.md) | Optional | The behavior of the finding reporting: Monitor / Comment / Block.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| MODE_MONITOR \| Monitor mode, silently report findings \|<br>\| MODE_COMMENT \| Comment mode, leaves PR comments but does not block \|<br>\| MODE_BLOCK \| Block mode, leaves PR comments and blocks PR \|<br>\| MODE_DISABLED \| Disabled mode, not active \| |
| `Ref` | `string` | Optional | Branch where the finding was detected. |
| `RefUrl` | `string` | Optional | URL to the branch where the finding was detected. |
| `Repository` | [`ProtosSecretsV1SecretsFindingRepository`](../../doc/models/protos-secrets-v1-secrets-finding-repository.md) | Optional | Repository where the finding was detected. |
| `ReviewComments` | [`List<ProtosCommonV1ReviewComment>`](../../doc/models/protos-common-v1-review-comment.md) | Optional | List of external review comment information associated with a finding |
| `RuleHashId` | `string` | Optional | ID of the rule that triggered the finding. |
| `Severity` | [`Severity4?`](../../doc/models/severity-4.md) | Optional | Severity of the finding.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SEVERITY_HIGH \|  \|<br>\| SEVERITY_MEDIUM \|  \|<br>\| SEVERITY_LOW \|  \|<br>\| SEVERITY_CRITICAL \|  \| |
| `Status` | [`Status6?`](../../doc/models/status-6.md) | Optional | Status of the finding.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| FINDING_STATUS_OPEN \|  \|<br>\| FINDING_STATUS_IGNORED \|  \|<br>\| FINDING_STATUS_FIXED \|  \|<br>\| FINDING_STATUS_REMOVED \|  \|<br>\| FINDING_STATUS_UNKNOWN \|  \|<br>\| FINDING_STATUS_PROVISIONALLY_IGNORED \|  \| |
| `Type` | `string` | Optional | Service type for the secrets finding (e.g. AWS, GitHub, GitLab, etc). |
| `UpdatedAt` | `DateTime?` | Optional | Update timestamp. |
| `ValidationState` | [`ValidationState2?`](../../doc/models/validation-state-2.md) | Optional | Whether the finding was validated or not.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| VALIDATION_STATE_CONFIRMED_VALID \|  \|<br>\| VALIDATION_STATE_CONFIRMED_INVALID \|  \|<br>\| VALIDATION_STATE_VALIDATION_ERROR \|  \|<br>\| VALIDATION_STATE_NO_VALIDATOR \|  \| |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

ProtosSecretsV1SecretsFinding protosSecretsV1SecretsFinding = new ProtosSecretsV1SecretsFinding
{
    Autotriage = new ProtosAiV1Autotriage
    {
        Feedback = new ProtosAiV1AutotriageFeedback
        {
            AutotriageId = "autotriageId0",
            Note = "note2",
            Rating = Rating.RatingGood,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Id = "id2",
        IssueId = "issueId0",
        MatchBasedId = "matchBasedId6",
        MemoryIdsReferenced = new List<string>
        {
            "memoryIdsReferenced4",
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Confidence = Confidence7.ConfidenceLow,
    CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ExternalTicket = new ProtosTicketingV1ExternalTicket
    {
        ExternalSlug = "externalSlug6",
        Id = "id6",
        LinkedIssueIds = new List<string>
        {
            "linkedIssueIds7",
        },
        Url = "url0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    FindingPath = "findingPath2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

