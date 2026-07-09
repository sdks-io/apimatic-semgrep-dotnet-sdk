
# Protos Openapi V1 List Policy Rules Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1ListPolicyRulesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cursor` | `string` | Optional | Cursor to paginate through the rules. |
| `Policy` | [`Policy`](../../doc/models/policy.md) | Optional | - |
| `Rules` | [`List<Rule>`](../../doc/models/rule.md) | Optional | List of Rules for the given Policy. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

ProtosOpenapiV1ListPolicyRulesResponse protosOpenapiV1ListPolicyRulesResponse = new ProtosOpenapiV1ListPolicyRulesResponse
{
    Cursor = "Pm0ROjIwMjQtMDItMDYgMjA6MDQ6NDguMEDzNzk2fmk6NYTM2zUxOTI",
    Policy = new Policy
    {
        Id = "id4",
        IsDefault = false,
        Name = "name4",
        ProductType = ProductType.ProductTypeSast,
        Slug = "slug8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Rules = new List<Rule>
    {
        new Rule
        {
            Category = "security",
            Confidence = Confidence.ConfidenceHigh,
            CweCategories = new List<string>
            {
                "CWE-918: Server-Side Request Forgery (SSRF)",
            },
            HasValidators = false,
            Id = "1",
            Languages = new List<string>
            {
                "python",
            },
            LastChangeAt = DateTime.ParseExact("2024-07-29T22:33:37.380293Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            OwaspCategories = new List<string>
            {
                "A07: Cross-Site Scripting (XSS)",
            },
            Path = "python.rule.1",
            PolicyMode = PolicyMode.ModeMonitor,
            RegistryMaintainer = "semgrep",
            Rulesets = new List<string>
            {

            },
            Severity = Severity.SeverityHigh,
            Source = Source.SourceCommunity,
            Technologies = new List<string>
            {
                "django",
                "flask",
            },
            Url = "https://semgrep.com/r/123/python.rule.1",
            VulnerabilityClass = new List<string>
            {
                "Improper Authentication",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Rule
        {
            Category = "security",
            Confidence = Confidence.ConfidenceHigh,
            CweCategories = new List<string>
            {
                "CWE-918: Server-Side Request Forgery (SSRF)",
            },
            HasValidators = false,
            Id = "2",
            Languages = new List<string>
            {
                "python",
            },
            LastChangeAt = DateTime.ParseExact("2024-07-29T22:33:37.380293Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            OwaspCategories = new List<string>
            {
                "A01:2021 - Broken Access Control",
                "A07: Cross-Site Scripting (XSS)",
            },
            Path = "python.rule.shared",
            PolicyMode = PolicyMode.ModeComment,
            RegistryMaintainer = "semgrep",
            Rulesets = new List<string>
            {
                "comment",
                "default",
            },
            Severity = Severity.SeverityMedium,
            Source = Source.SourcePro,
            Technologies = new List<string>
            {
                "django",
                "flask",
            },
            Url = "https://semgrep.com/r/123/python.rule.shared",
            VulnerabilityClass = new List<string>
            {
                "Improper Authentication",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Rule
        {
            Category = "best-practice",
            Confidence = Confidence.ConfidenceHigh,
            CweCategories = new List<string>
            {

            },
            HasValidators = false,
            Id = "3",
            Languages = new List<string>
            {
                "python",
            },
            LastChangeAt = DateTime.ParseExact("2024-07-29T22:33:37.380293Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            LastChangeBy = "example-user",
            OwaspCategories = new List<string>
            {

            },
            Path = "python.rule.custom_rule",
            PolicyMode = PolicyMode.ModeBlock,
            RegistryMaintainer = "semgrep",
            Rulesets = new List<string>
            {

            },
            Severity = Severity.SeverityMedium,
            Source = Source.SourceCustom,
            Technologies = new List<string>
            {
                "django",
                "flask",
            },
            Url = "https://semgrep.com/r/123/python.rule.custom_rule",
            VulnerabilityClass = new List<string>
            {
                "Improper Authentication",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

