
# List Dependencies Response

*This model accepts additional fields of type object.*

## Structure

`ListDependenciesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cursor` | `string` | Optional | Pass to next request to get next page of results. |
| `Dependencies` | [`List<ProtosScaV1FoundDependency>`](../../doc/models/protos-sca-v1-found-dependency.md) | Required | List of dependencies. |
| `HasMore` | `bool` | Required | True if there are more dependencies to get. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

ListDependenciesResponse listDependenciesResponse = new ListDependenciesResponse
{
    Dependencies = new List<ProtosScaV1FoundDependency>
    {
        new ProtosScaV1FoundDependency
        {
            DefinedAt = new ProtosScaV1CodeLocation
            {
                CommittedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                EndCol = "endCol8",
                EndLine = "endLine2",
                Path = "path2",
                StartCol = "startCol2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Ecosystem = Ecosystem1.Cocoapods,
            Licenses = new List<string>
            {
                "licenses3",
                "licenses4",
                "licenses5",
            },
            ManifestDefinition = new ProtosScaV1CodeLocation
            {
                CommittedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                EndCol = "endCol0",
                EndLine = "endLine4",
                Path = "path4",
                StartCol = "startCol4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Package = new ProtosScaV1Dependency
            {
                Name = "name8",
                VersionSpecifier = "versionSpecifier6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["id"] = ApiHelper.JsonDeserialize<object>("\"1\""),
            ["name"] = ApiHelper.JsonDeserialize<object>("\"dependency1\""),
            ["version"] = ApiHelper.JsonDeserialize<object>("\"1.0.0\""),
        },
        new ProtosScaV1FoundDependency
        {
            DefinedAt = new ProtosScaV1CodeLocation
            {
                CommittedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                EndCol = "endCol8",
                EndLine = "endLine2",
                Path = "path2",
                StartCol = "startCol2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Ecosystem = Ecosystem1.Cocoapods,
            Licenses = new List<string>
            {
                "licenses3",
                "licenses4",
                "licenses5",
            },
            ManifestDefinition = new ProtosScaV1CodeLocation
            {
                CommittedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                EndCol = "endCol0",
                EndLine = "endLine4",
                Path = "path4",
                StartCol = "startCol4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Package = new ProtosScaV1Dependency
            {
                Name = "name8",
                VersionSpecifier = "versionSpecifier6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["id"] = ApiHelper.JsonDeserialize<object>("\"2\""),
            ["name"] = ApiHelper.JsonDeserialize<object>("\"dependency2\""),
            ["version"] = ApiHelper.JsonDeserialize<object>("\"2.0.0\""),
        },
    },
    HasMore = false,
    Cursor = "cursor2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

