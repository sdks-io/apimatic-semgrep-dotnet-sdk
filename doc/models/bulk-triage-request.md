
# Bulk Triage Request

*This model accepts additional fields of type object.*

## Structure

`BulkTriageRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutotriageVerdict` | [`AutotriageVerdict?`](../../doc/models/autotriage-verdict.md) | Optional | The autotriage verdict to filter by |
| `Categories` | `List<string>` | Optional | List of categories to filter by |
| `ComponentTags` | `List<string>` | Optional | List of component tags to filter by |
| `Confidence` | [`Confidence3?`](../../doc/models/confidence-3.md) | Optional | List of confidence levels to filter by |
| `Dependencies` | `List<string>` | Optional | Filter by dependency name. Only applies for sca findings. |
| `EpssProbability` | [`EpssProbability?`](../../doc/models/epss-probability.md) | Optional | Filter by EPSS probability (likelihood of exploit). Only applies for sca findings. |
| `Exposures` | [`Exposures?`](../../doc/models/exposures.md) | Optional | Filter by exposure (reachability type). Only applies for sca findings. Reachability is the ability of an attacker to access a vulnerability in a system. |
| `IncludeHistorical` | `bool?` | Optional | Whether to include historical findings. Only applies for secrets findings. Defaults to true. |
| `IssueIds` | `List<long>` | Optional | An array of issue IDs to act on. If this is not provided, an issue filter should be provided. |
| `IssueType` | [`IssueType`](../../doc/models/issue-type.md) | Required | Type of findings to bulk triage. |
| `Limit` | `long?` | Optional | Max number of issues to triage. Must be an integer between 1 and 3000. Defaults to 3000. When selecting findings to triage, Semgrep will also triage findings with the same fingerprint on other branches. As a result, the list of triaged issue_ids returned in the response may be higher than the specified limit.<br><br>**Default**: `3000L` |
| `NewNote` | `string` | Optional | The note to attach to the bulk triaged findings. Maximum 3000 characters. |
| `NewTriageReason` | [`NewTriageReason?`](../../doc/models/new-triage-reason.md) | Optional | The reason for triaging to a given triage state. |
| `NewTriageState` | [`NewTriageState?`](../../doc/models/new-triage-state.md) | Optional | The triage state you would like to bulk triage your findings to. |
| `Policies` | `List<string>` | Optional | List of policy modes to filter by |
| `PolicyMode` | [`PolicyMode1?`](../../doc/models/policy-mode-1.md) | Optional | List of policy modes to filter by |
| `ProOnly` | `bool?` | Optional | Filter by whether a finding is only available with Semgrep Pro features. |
| `ProjectTags` | `List<string>` | Optional | List of project tags to filter by |
| `Ref` | `string` | Optional | Branch reference to filter by |
| `Repos` | `List<string>` | Optional | List of repository names to filter by |
| `RepositoryVisibility` | [`RepositoryVisibility?`](../../doc/models/repository-visibility.md) | Optional | Filter by repository visibility. Only applies for secrets findings. |
| `Rules` | `List<string>` | Optional | List of rule names to filter by |
| `Ruleset` | `List<string>` | Optional | List of Semgrep Registry rulesets to filter by |
| `SecretTypes` | `List<string>` | Optional | Filter by type of secret (typically provider-related). Only applies for secrets findings. |
| `Severities` | [`Severities?`](../../doc/models/severities.md) | Optional | List of severities to filter by |
| `Since` | `string` | Optional | Epoch timestamp in seconds. Filters using the relevant_since field: the timestamp when this finding was detected by Semgrep (the first time, or when reintroduced). |
| `Status` | [`Status1?`](../../doc/models/status-1.md) | Optional | The status to filter by |
| `Transitivities` | [`Transitivities?`](../../doc/models/transitivities.md) | Optional | Filter by transitivity of a dependency. Only applies for sca findings. |
| `TriageReasons` | [`TriageReasons?`](../../doc/models/triage-reasons.md) | Optional | List of triage reasons to filter by |
| `ValidationState` | [`ValidationState?`](../../doc/models/validation-state.md) | Optional | Filter by whether a secret could be validated. Only applies for secrets findings. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

BulkTriageRequest bulkTriageRequest = new BulkTriageRequest
{
    IssueType = IssueType.Sca,
    AutotriageVerdict = AutotriageVerdict.TruePositive,
    Categories = new List<string>
    {
        "security",
        "performance",
    },
    ComponentTags = new List<string>
    {
        "user authentication",
        "user data",
    },
    Confidence = Confidence3.High,
    Dependencies = new List<string>
    {
        "lodash",
        "express",
    },
    IncludeHistorical = true,
    IssueIds = new List<long>
    {
        123L,
        456L,
    },
    Limit = 100L,
    NewNote = "some note here",
    NewTriageReason = NewTriageReason.AcceptableRisk,
    NewTriageState = NewTriageState.Reopened,
    Policies = new List<string>
    {
        "rule-board-block",
        "rule-board-pr-comments",
        "rule-board-audit",
    },
    ProOnly = true,
    ProjectTags = new List<string>
    {
        "my_project_tag_1",
        "my_project_tag_2",
    },
    MRef = "refs/pull/1234/merge",
    Repos = new List<string>
    {
        "myorg/repo1",
        "myorg/repo2",
    },
    Rules = new List<string>
    {
        "typescript.react.security.audit.react-no-refs.react-no-refs",
        "ajinabraham.njsscan.hardcoded_secrets.node_username",
    },
    Ruleset = new List<string>
    {
        "owasp-top-ten",
        "default",
    },
    SecretTypes = new List<string>
    {
        "Github",
        "Heroku",
        "AWS",
    },
    Since = "1717334400",
    Status = Status1.Open,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

