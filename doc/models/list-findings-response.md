
# List Findings Response

Response containing a paginated list of findings (either Code or Supply Chain findings) with optional filtering applied

*This model accepts additional fields of type object.*

## Structure

`ListFindingsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AiSastFindings` | [`AiSastFindings`](../../doc/models/ai-sast-findings.md) | Optional | A list of AI-powered scan findings that Semgrep has identified in your organization |
| `SastFindings` | [`SastFindings`](../../doc/models/sast-findings.md) | Optional | A list of Code findings that Semgrep has identified in your organization |
| `ScaFindings` | [`ScaFindings`](../../doc/models/sca-findings.md) | Optional | A list of Supply Chain findings that Semgrep has identified in your organization |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ListFindingsResponse listFindingsResponse = new ListFindingsResponse
{
    AiSastFindings = new AiSastFindings
    {
        Findings = new List<AiPoweredScanFinding>
        {
            new AiPoweredScanFinding
            {
                AiImpact = "ai_impact2",
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
                },
                ClickToFixPrs = new List<ClickToFixPr>
                {
                    new ClickToFixPr
                    {
                        CreatedAt = "created_at4",
                        Url = "url0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Confidence = Confidence1.Low,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new AiPoweredScanFinding
            {
                AiImpact = "ai_impact2",
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
                },
                ClickToFixPrs = new List<ClickToFixPr>
                {
                    new ClickToFixPr
                    {
                        CreatedAt = "created_at4",
                        Url = "url0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Confidence = Confidence1.Low,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new AiPoweredScanFinding
            {
                AiImpact = "ai_impact2",
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
                },
                ClickToFixPrs = new List<ClickToFixPr>
                {
                    new ClickToFixPr
                    {
                        CreatedAt = "created_at4",
                        Url = "url0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Confidence = Confidence1.Low,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    SastFindings = new SastFindings
    {
        Findings = new List<SastFinding>
        {
            new SastFinding
            {
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
                Categories = new List<string>
                {
                    "categories4",
                    "categories3",
                },
                ClickToFixFailures = new List<ClickToFixFailure>
                {
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
                },
                Confidence = Confidence1.Low,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new SastFinding
            {
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
                Categories = new List<string>
                {
                    "categories4",
                    "categories3",
                },
                ClickToFixFailures = new List<ClickToFixFailure>
                {
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
                },
                Confidence = Confidence1.Low,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ScaFindings = new ScaFindings
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
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

