
# Sca Findings

A list of Supply Chain findings that Semgrep has identified in your organization

*This model accepts additional fields of type object.*

## Structure

`ScaFindings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Findings` | [`List<ScaFinding>`](../../doc/models/sca-finding.md) | Optional | A list of Supply Chain findings. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ScaFindings scaFindings = new ScaFindings
{
    Findings = new List<ScaFinding>
    {
        new ScaFinding
        {
            Categories = new List<string>
            {
                "categories4",
                "categories3",
            },
            Confidence = Confidence1.Low,
            CreatedAt = "created_at6",
            EpssScore = new EpssScore
            {
                Percentile = 236.52,
                Score = 242.58,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ExternalTicket = new ExternalTicket
            {
                ExternalSlug = "external_slug4",
                Id = 228L,
                LinkedIssueIds = new List<long>
                {
                    115L,
                    116L,
                    117L,
                },
                Url = "url8",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ScaFinding
        {
            Categories = new List<string>
            {
                "categories4",
                "categories3",
            },
            Confidence = Confidence1.Low,
            CreatedAt = "created_at6",
            EpssScore = new EpssScore
            {
                Percentile = 236.52,
                Score = 242.58,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ExternalTicket = new ExternalTicket
            {
                ExternalSlug = "external_slug4",
                Id = 228L,
                LinkedIssueIds = new List<long>
                {
                    115L,
                    116L,
                    117L,
                },
                Url = "url8",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ScaFinding
        {
            Categories = new List<string>
            {
                "categories4",
                "categories3",
            },
            Confidence = Confidence1.Low,
            CreatedAt = "created_at6",
            EpssScore = new EpssScore
            {
                Percentile = 236.52,
                Score = 242.58,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ExternalTicket = new ExternalTicket
            {
                ExternalSlug = "external_slug4",
                Id = 228L,
                LinkedIssueIds = new List<long>
                {
                    115L,
                    116L,
                    117L,
                },
                Url = "url8",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

