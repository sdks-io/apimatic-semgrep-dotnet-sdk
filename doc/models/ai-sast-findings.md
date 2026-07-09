
# Ai Sast Findings

A list of AI-powered scan findings that Semgrep has identified in your organization

*This model accepts additional fields of type object.*

## Structure

`AiSastFindings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Findings` | [`List<AiPoweredScanFinding>`](../../doc/models/ai-powered-scan-finding.md) | Optional | A list of AI-powered scan findings. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

AiSastFindings aiSastFindings = new AiSastFindings
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
};
```

