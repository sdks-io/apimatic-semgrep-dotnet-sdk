
# Api V1 Deployments Findings Response

*This model accepts additional fields of type object.*

## Structure

`ApiV1DeploymentsFindingsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Findings` | [`List<ApiV1DeploymentsFindingsResponseFindings>`](../../doc/models/containers/api-v1-deployments-findings-response-findings.md) | Optional | This is List of a container for one-of cases. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Models.Containers;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ApiV1DeploymentsFindingsResponse apiV1DeploymentsFindingsResponse = new ApiV1DeploymentsFindingsResponse
{
    Findings = new List<ApiV1DeploymentsFindingsResponseFindings>
    {
        ApiV1DeploymentsFindingsResponseFindings.FromSastFinding(
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
                },
                ClickToFixFailures = new List<ClickToFixFailure>
                {
                    new ClickToFixFailure
                    {
                        CreatedAt = "created_at8",
                        Reason = "reason0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new ClickToFixFailure
                    {
                        CreatedAt = "created_at8",
                        Reason = "reason0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
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
                    new ClickToFixPr
                    {
                        CreatedAt = "created_at4",
                        Url = "url0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new ClickToFixPr
                    {
                        CreatedAt = "created_at4",
                        Url = "url0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Confidence = Confidence1.High,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
        ApiV1DeploymentsFindingsResponseFindings.FromSastFinding(
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
                },
                ClickToFixFailures = new List<ClickToFixFailure>
                {
                    new ClickToFixFailure
                    {
                        CreatedAt = "created_at8",
                        Reason = "reason0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new ClickToFixFailure
                    {
                        CreatedAt = "created_at8",
                        Reason = "reason0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
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
                    new ClickToFixPr
                    {
                        CreatedAt = "created_at4",
                        Url = "url0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new ClickToFixPr
                    {
                        CreatedAt = "created_at4",
                        Url = "url0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Confidence = Confidence1.High,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
        ApiV1DeploymentsFindingsResponseFindings.FromSastFinding(
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
                },
                ClickToFixFailures = new List<ClickToFixFailure>
                {
                    new ClickToFixFailure
                    {
                        CreatedAt = "created_at8",
                        Reason = "reason0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new ClickToFixFailure
                    {
                        CreatedAt = "created_at8",
                        Reason = "reason0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
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
                    new ClickToFixPr
                    {
                        CreatedAt = "created_at4",
                        Url = "url0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new ClickToFixPr
                    {
                        CreatedAt = "created_at4",
                        Url = "url0",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Confidence = Confidence1.High,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

