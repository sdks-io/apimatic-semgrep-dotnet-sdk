
# Protos Secrets V1 Secrets Finding Repository

Repository where the finding was detected.

*This model accepts additional fields of type object.*

## Structure

`ProtosSecretsV1SecretsFindingRepository`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Optional | Repository name |
| `ScmType` | [`ScmType?`](../../doc/models/scm-type.md) | Optional | Provider for the finding (e.g. GitHub, GitLab, GHE, etc).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SCM_TYPE_GITHUB \| GitHub Cloud \|<br>\| SCM_TYPE_GITHUB_ENTERPRISE \| GitHub Enterprise \|<br>\| SCM_TYPE_GITLAB \| GitLab Cloud \|<br>\| SCM_TYPE_GITLAB_SELFMANAGED \| GitLab Self-Managed \|<br>\| SCM_TYPE_BITBUCKET \| Bitbucket Cloud \|<br>\| SCM_TYPE_BITBUCKET_DATACENTER \| Bitbucket Data Center \|<br>\| SCM_TYPE_AZURE_DEVOPS \| Azure DevOps \|<br>\| SCM_TYPE_UNKNOWN \|  \|<br>\| SCM_TYPE_HARNESS \| Harness \| |
| `Url` | `string` | Optional | URL to the repository where the finding was detected. |
| `Visibility` | [`Visibility?`](../../doc/models/visibility.md) | Optional | Repository visbility (e.g. public, private, unknown).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| REPOSITORY_VISIBILITY_PUBLIC \|  \|<br>\| REPOSITORY_VISIBILITY_PRIVATE \|  \|<br>\| REPOSITORY_VISIBILITY_UNKNOWN \|  \| |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosSecretsV1SecretsFindingRepository protosSecretsV1SecretsFindingRepository = new ProtosSecretsV1SecretsFindingRepository
{
    Name = "name4",
    ScmType = ScmType.ScmTypeBitbucketDatacenter,
    Url = "url8",
    Visibility = Visibility.RepositoryVisibilityPrivate,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

