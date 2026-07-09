
# Protos Secrets V1 Historical Info

*This model accepts additional fields of type object.*

## Structure

`ProtosSecretsV1HistoricalInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `GitBlob` | `string` | Optional | Git blob at which the finding is present. Sent in addition to the commit<br>since some SCMs have permalinks which use the blob sha, so this information<br>is useful when generating links back to the SCM. |
| `GitCommit` | `string` | Optional | Git commit at which the finding is present. Used by "historical" scans,<br>which scan non-HEAD commits in the git history. Relevant for finding, e.g.,<br>secrets which are buried in the git history which we wouldn't find at HEAD |
| `GitCommitTimestamp` | `DateTime?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Globalization;

ProtosSecretsV1HistoricalInfo protosSecretsV1HistoricalInfo = new ProtosSecretsV1HistoricalInfo
{
    GitBlob = "gitBlob8",
    GitCommit = "gitCommit2",
    GitCommitTimestamp = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

