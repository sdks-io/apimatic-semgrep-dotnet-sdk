
# Protos Openapi V1 Get Scan Response Scan Meta

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1GetScanResponseScanMeta`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `True` | `string` | Optional | What triggered this scan, if applicable. |
| `Branch` | `string` | Optional | The branch that was scanned, if applicable. |
| `Commit` | `string` | Optional | The commit SHA associated with the scan, if applicable. |
| `Config` | `string` | Optional | The path of the configuration file used for this scan, if applicable. |
| `RepoUrl` | `string` | Optional | The URL of the scanned repository, if applicable. |
| `CiJobUrl` | `string` | Optional | The URL of the CI job that ran the scan, if applicable. |
| `Repository` | `string` | Optional | The name and organization of the scanned repository, if applicable. |
| `CommitTitle` | `string` | Optional | The commit message associated with the scan, if applicable. |
| `PullRequestId` | `string` | Optional | The ID of the pull request associated with the scan, if applicable. |
| `PullRequestTitle` | `string` | Optional | The title of the pull request associated with the scan if applicable. |
| `CommitAuthorName` | `string` | Optional | The name of the author of the commit associated with the scan, if applicable. |
| `CommitAuthorImageUrl` | `string` | Optional | The avatar image url of the author of the commit associated with the scan, if applicable. |
| `CommitAuthorEmail` | `string` | Optional | The email of the author of the commit associated with the scan, if applicable. |
| `CommitAuthorUsername` | `string` | Optional | The username of the author of the commit associated with the scan, if applicable. |
| `PullRequestAuthorUsername` | `string` | Optional | The username of the author of the pull request associated with the scan, if applicable. |
| `PullRequestAuthorImageUrl` | `string` | Optional | The avatar image url of the author of the pull request associated with the scan, if applicable. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosOpenapiV1GetScanResponseScanMeta protosOpenapiV1GetScanResponseScanMeta = new ProtosOpenapiV1GetScanResponseScanMeta
{
    MTrue = "pull_request",
    Branch = "refs/heads/main",
    Commit = "94c5be1312a9da03b7c4bfcc1c50b4379c83412",
    Config = "r/python",
    RepoUrl = "https://github.com/semgrep/semgrep",
    CiJobUrl = "https://github.com/semgrep/semgrep/actions/runs/12345",
    Repository = "semgrep/semgrep",
    CommitTitle = "{\n  \"fix(feature)\": \"Added XYZ component\"\n}",
    PullRequestId = "12345",
    PullRequestTitle = "{\n  \"fix(feature)\": \"Added XYZ component\"\n}",
    CommitAuthorName = "Sven Greppe",
    CommitAuthorImageUrl = "https://github.com/link/to/avatar.png",
    CommitAuthorEmail = "sven.greppe@semgrep.com",
    CommitAuthorUsername = "SvenGreppe",
    PullRequestAuthorUsername = "SvenGreppe",
    PullRequestAuthorImageUrl = "https://github.com/link/to/avatar.png",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

