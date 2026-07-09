
# Protos Openapi V1 List Secrets Path Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1ListSecretsPathResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cursor` | `string` | Optional | Cursor to paginate through the results. |
| `Findings` | [`List<ProtosSecretsV1SecretsFinding>`](../../doc/models/protos-secrets-v1-secrets-finding.md) | Optional | List of Secrets associated with the given Deployment. |
| `Previous` | `string` | Optional | Cursor to paginate backwards through the results. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

ProtosOpenapiV1ListSecretsPathResponse protosOpenapiV1ListSecretsPathResponse = new ProtosOpenapiV1ListSecretsPathResponse
{
    Cursor = "cursor4",
    Findings = new List<ProtosSecretsV1SecretsFinding>
    {
        new ProtosSecretsV1SecretsFinding
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
            Confidence = Confidence7.ConfidenceHigh,
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
            FindingPath = "findingPath8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ProtosSecretsV1SecretsFinding
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
            Confidence = Confidence7.ConfidenceHigh,
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
            FindingPath = "findingPath8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Previous = "previous0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

