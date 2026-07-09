
# Ai Powered Scan Finding

An AI-powered scan finding that Semgrep has identified in your organization

*This model accepts additional fields of type object.*

## Structure

`AiPoweredScanFinding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AiImpact` | `string` | Optional | AI-generated description of the potential impact if this vulnerability is exploited |
| `Assistant` | [`Assistant`](../../doc/models/assistant.md) | Optional | Semgrep Assistant data. Only present if Assistant is enabled |
| `ClickToFixFailures` | [`List<ClickToFixFailure>`](../../doc/models/click-to-fix-failure.md) | Optional | Failed PR creation attempts by Semgrep's autofix feature (Click to Fix) for this finding |
| `ClickToFixPrs` | [`List<ClickToFixPr>`](../../doc/models/click-to-fix-pr.md) | Optional | Pull requests created by Semgrep's autofix feature (Click to Fix) for this finding |
| `Confidence` | [`Confidence1?`](../../doc/models/confidence-1.md) | Optional | Confidence of the finding, derived from the rule that triggered it |
| `CreatedAt` | `string` | Optional | The timestamp when this finding was created |
| `ExternalTicket` | [`ExternalTicket`](../../doc/models/external-ticket.md) | Optional | External ticket associated with finding |
| `FirstSeenScanId` | `long?` | Optional | Unique ID of the Semgrep scan that first identified this finding |
| `Id` | `long?` | Optional | Unique ID of this finding |
| `LineOfCodeUrl` | `string` | Optional | The source URL including file and line number |
| `Location` | [`FindingLocation`](../../doc/models/finding-location.md) | Optional | Location of the record in a file, as reported by Semgrep. If null, then the information does not exist or lacks integrity (older or broken scans) |
| `MatchBasedId` | `string` | Optional | ID calculated based on a finding's file path, rule identifier and pattern, and index |
| `Ref` | `string` | Optional | External reference to the source of this finding (e.g. PR) |
| `RelevantSince` | `string` | Optional | The timestamp when this finding was detected by Semgrep (the first time, or when reintroduced) |
| `Repository` | [`FindingRepository`](../../doc/models/finding-repository.md) | Optional | Which repository this finding was identified in |
| `ReviewComments` | [`List<ReviewComment>`](../../doc/models/review-comment.md) | Optional | List of external review comment information associated with a finding |
| `Rule` | [`FindingRule`](../../doc/models/finding-rule.md) | Optional | Rule that applies to this finding |
| `RuleMessage` | `string` | Optional | Deprecated in favor of rule.message. Rule message at the time of finding identification. Older findings may not have a value for this field |
| `RuleName` | `string` | Optional | Deprecated in favor of rule.name |
| `Severity` | [`Severity1?`](../../doc/models/severity-1.md) | Optional | Severity of the finding, derived from the rule that triggered it. Low is equivalent to INFO, Medium to WARNING, and High to ERROR |
| `SourcingPolicy` | [`PolicyReference`](../../doc/models/policy-reference.md) | Optional | Reference to a policy, with some basic information. If null, then the information does not exist or lacks integrity (older or broken scans) |
| `State` | [`State?`](../../doc/models/state.md) | Optional | The finding's resolution state. Managed only by changes detected at scan time, the `state` is combined with `triage_state` to ultimately determine a final `status` which is exposed in the UI and API |
| `StateUpdatedAt` | `string` | Optional | When this issue's `state` (resolution state) was last updated, as distinct from when the issue was triaged (`triaged_at`) |
| `Status` | [`Status?`](../../doc/models/status.md) | Optional | The finding's status as exposed in the UI. Status is a derived property combining information from the finding `state` and `triage_state`. The `triage_state` can be used to override the scan state if the finding is still detected |
| `SyntacticId` | `string` | Optional | ID calculated based on a finding's file path, rule identifier and matched code, and index. Prefer `match_based_id` |
| `TriageComment` | `string` | Optional | The detailed comment provided during triage |
| `TriageReason` | [`TriageReason?`](../../doc/models/triage-reason.md) | Optional | Reason provided when this issue was triaged |
| `TriageState` | [`TriageState?`](../../doc/models/triage-state.md) | Optional | The finding's triage state. Note: "reviewing" and "fixing" are only in private beta. Set by the user and used along with state to generate the final "status" viewable in the UI |
| `TriagedAt` | `string` | Optional | When the finding was triaged |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

AiPoweredScanFinding aiPoweredScanFinding = new AiPoweredScanFinding
{
    AiImpact = "An attacker could access or modify other users' data by manipulating the resource identifier in the request",
    Assistant = new Assistant
    {
        Autofix = new Autofix
        {
            Explanation = "explanation2",
            FixCode = "fix_code4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Autotriage = new Autotriage
        {
            Reason = "reason2",
            Verdict = Verdict1.FalsePositive,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Component = new Component
        {
            Risk = Risk.High,
            Tag = "tag8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Guidance = new Guidance
        {
            Instructions = "instructions4",
            Summary = "summary8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        RuleExplanation = new RuleExplanation
        {
            Explanation = "explanation8",
            Summary = "summary4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ClickToFixFailures = new List<ClickToFixFailure>
    {
        new ClickToFixFailure
        {
            CreatedAt = "created_at8",
            Reason = "reason0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ClickToFixFailure
        {
            CreatedAt = "created_at8",
            Reason = "reason0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ClickToFixFailure
        {
            CreatedAt = "created_at8",
            Reason = "reason0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ClickToFixPrs = new List<ClickToFixPr>
    {
        new ClickToFixPr
        {
            CreatedAt = "created_at4",
            Url = "url0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ClickToFixPr
        {
            CreatedAt = "created_at4",
            Url = "url0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ClickToFixPr
        {
            CreatedAt = "created_at4",
            Url = "url0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Confidence = Confidence1.Medium,
    CreatedAt = "2020-11-18 23:28:12.391807+00:00",
    FirstSeenScanId = 1234L,
    Id = 1234567L,
    LineOfCodeUrl = "https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1",
    MatchBasedId = "0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1",
    MRef = "refs/pull/1234/merge",
    RelevantSince = "2020-11-18 23:28:12.391807+00:00",
    RuleName = "ai.detection.idor",
    Severity = Severity1.High,
    State = State.Unresolved,
    StateUpdatedAt = "2020-11-19 23:28:12.391807+00:00",
    Status = Status.Open,
    SyntacticId = "440eeface888e78afceac3dc7d4cc2cf",
    TriageComment = "This finding is from the test repo",
    TriageReason = TriageReason.AcceptableRisk,
    TriageState = TriageState.Untriaged,
    TriagedAt = "2020-11-19 23:28:12.391807+00:00",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

