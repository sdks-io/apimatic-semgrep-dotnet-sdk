# Findings Service

Manage and retrieve code, supply chain, and AI-powered scan findings from Semgrep scans

```csharp
FindingsServiceApi findingsServiceApi = client.FindingsServiceApi;
```

## Class Name

`FindingsServiceApi`


# List Findings

Request the list of code, supply chain, or AI-powered scan findings in an organization, paginated in pages of 100 entries and limited by the `since` timestamp. Findings are returned by `relevant_since` descending (see `since` in the Query Parameters list). Examples: List SAST findings with pagination, List SCA findings since timestamp, List AI-powered scan findings, List findings with filters.

```csharp
ListFindingsAsync(
    string deploymentSlug,
    Models.IssueType2? issueType = Models.IssueType2.Sast,
    double? since = null,
    long? page = 0L,
    bool? dedup = false,
    long? pageSize = 100L,
    List<string> repos = null,
    List<long> repositoryIds = null,
    Models.Status9? status = null,
    Models.TriageReasons2? triageReasons = null,
    Models.Severities2? severities = null,
    string mRef = null,
    List<string> policies = null,
    List<string> rules = null,
    List<string> categories = null,
    Models.Confidence8? confidence = null,
    Models.AutotriageVerdict2? autotriageVerdict = null,
    List<string> componentTags = null,
    Models.Exposures2? exposures = null,
    Models.Transitivities2? transitivities = null,
    bool? isMalicious = null,
    Models.ClickToFixPrState? clickToFixPrState = null)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `issueType` | [`IssueType2?`](../../doc/models/issue-type-2.md) | Query, Optional | **Default**: `IssueType2.sast` |
| `since` | `double?` | Query, Optional | - |
| `page` | `long?` | Query, Optional | **Default**: `0L` |
| `dedup` | `bool?` | Query, Optional | **Default**: `false` |
| `pageSize` | `long?` | Query, Optional | **Default**: `100L`<br><br>**Constraints**: `>= 100`, `<= 3000` |
| `repos` | `List<string>` | Query, Optional | - |
| `repositoryIds` | `List<long>` | Query, Optional | - |
| `status` | [`Status9?`](../../doc/models/status-9.md) | Query, Optional | - |
| `triageReasons` | [`TriageReasons2?`](../../doc/models/triage-reasons-2.md) | Query, Optional | - |
| `severities` | [`Severities2?`](../../doc/models/severities-2.md) | Query, Optional | - |
| `mRef` | `string` | Query, Optional | - |
| `policies` | `List<string>` | Query, Optional | - |
| `rules` | `List<string>` | Query, Optional | - |
| `categories` | `List<string>` | Query, Optional | - |
| `confidence` | [`Confidence8?`](../../doc/models/confidence-8.md) | Query, Optional | - |
| `autotriageVerdict` | [`AutotriageVerdict2?`](../../doc/models/autotriage-verdict-2.md) | Query, Optional | - |
| `componentTags` | `List<string>` | Query, Optional | - |
| `exposures` | [`Exposures2?`](../../doc/models/exposures-2.md) | Query, Optional | - |
| `transitivities` | [`Transitivities2?`](../../doc/models/transitivities-2.md) | Query, Optional | - |
| `isMalicious` | `bool?` | Query, Optional | - |
| `clickToFixPrState` | [`ClickToFixPrState?`](../../doc/models/click-to-fix-pr-state.md) | Query, Optional | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ApiV1DeploymentsFindingsResponse](../../doc/models/api-v1-deployments-findings-response.md).

## Example Usage

```csharp
string deploymentSlug = "your-deployment";
IssueType2? issueType = IssueType2.Sca;
double? since = 1636942398.45;
long? page = 1L;
bool? dedup = true;
long? pageSize = 100L;
List<string> repos = new List<string>
{
    "myorg/repo1",
    "myorg/repo2",
};

List<long> repositoryIds = new List<long>
{
    1L,
    2L,
    3L,
};

Status9? status = Status9.Open;
string mRef = "refs/pull/1234/merge";
List<string> policies = new List<string>
{
    "rule-board-block",
    "rule-board-pr-comments",
    "rule-board-audit",
};

List<string> rules = new List<string>
{
    "typescript.react.security.audit.react-no-refs.react-no-refs",
    "ajinabraham.njsscan.hardcoded_secrets.node_username",
};

List<string> categories = new List<string>
{
    "security",
    "correctness",
    "caching",
};

Confidence8? confidence = Confidence8.High;
AutotriageVerdict2? autotriageVerdict = AutotriageVerdict2.TruePositive;
List<string> componentTags = new List<string>
{
    "user authentication",
    "user data",
};

bool? isMalicious = true;
try
{
    ApiResponse<ApiV1DeploymentsFindingsResponse> result = await findingsServiceApi.ListFindingsAsync(
        deploymentSlug,
        issueType,
        since,
        page,
        dedup,
        pageSize,
        repos,
        repositoryIds,
        status,
        null,
        null,
        mRef,
        policies,
        rules,
        categories,
        confidence,
        autotriageVerdict,
        componentTags,
        null,
        null,
        isMalicious
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

