# Triage Service

View and manage the triage of your organization.

```csharp
TriageServiceApi triageServiceApi = client.TriageServiceApi;
```

## Class Name

`TriageServiceApi`


# Bulk Triage

Bulk triage your findings. You can select the findings to triage by passing in a list of finding IDs as issue_ids, or by passing in filter query parameters. You must specify the issue_type of the findings you want to bulk triage. One of new_triage_state or new_note is required. If specifying a new_triage_reason, you must also use new_triage_state=ignored. Some filters only apply for findings associated with a given product.

```csharp
BulkTriageAsync(
    string deploymentSlug,
    Models.BulkTriageRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `body` | [`BulkTriageRequest`](../../doc/models/bulk-triage-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.BulkTriageResponse](../../doc/models/bulk-triage-response.md).

## Example Usage

```csharp
string deploymentSlug = "deploymentSlug6";
BulkTriageRequest body = new BulkTriageRequest
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
};

try
{
    ApiResponse<BulkTriageResponse> result = await triageServiceApi.BulkTriageAsync(
        deploymentSlug,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

