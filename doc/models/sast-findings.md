
# Sast Findings

A list of Code findings that Semgrep has identified in your organization

*This model accepts additional fields of type object.*

## Structure

`SastFindings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Findings` | [`List<SastFinding>`](../../doc/models/sast-finding.md) | Optional | A list of Code findings. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

SastFindings sastFindings = new SastFindings
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
};
```

