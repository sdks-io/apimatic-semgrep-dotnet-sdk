
# Rule

*This model accepts additional fields of type object.*

## Structure

`Rule`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Category` | `string` | Optional | Category the Rule is associated with. |
| `Confidence` | [`Confidence?`](../../doc/models/confidence.md) | Optional | Confidence based on the Rule's false-positive rate.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| CONFIDENCE_HIGH \|  \|<br>\| CONFIDENCE_MEDIUM \|  \|<br>\| CONFIDENCE_LOW \|  \| |
| `CweCategories` | `List<string>` | Optional | The CWE associated with the Rule. |
| `HasValidators` | `bool?` | Optional | When True, the secrets rule has validators. |
| `Id` | `string` | Optional | ID of the Rule. |
| `Languages` | `List<string>` | Optional | Languages the Rule applies to. |
| `LastChangeAt` | `DateTime?` | Optional | Timestamp of when the Rule was last changed. |
| `LastChangeBy` | `string` | Optional | Username of who last changed the Rule. |
| `OwaspCategories` | `List<string>` | Optional | Owasp categories the Rule is associated with. |
| `Path` | `string` | Optional | Full path of the Rule. |
| `PolicyMode` | [`PolicyMode?`](../../doc/models/policy-mode.md) | Optional | Mode behavior: Monitor / Comment / Block / Disabled<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| MODE_MONITOR \| Monitor mode, silently report findings \|<br>\| MODE_COMMENT \| Comment mode, leaves PR comments but does not block \|<br>\| MODE_BLOCK \| Block mode, leaves PR comments and blocks PR \|<br>\| MODE_DISABLED \| Disabled mode, not active \| |
| `RegistryMaintainer` | `string` | Optional | The Registry maintainer associated with the Rule (if applicable). |
| `Rulesets` | `List<string>` | Optional | Rulesets to which the Rule belongs (if applicable). |
| `SecretType` | `string` | Optional | The secret type (if applicable). |
| `Severity` | [`Severity?`](../../doc/models/severity.md) | Optional | Severity level ("seriousness" of the finding)<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SEVERITY_HIGH \|  \|<br>\| SEVERITY_MEDIUM \|  \|<br>\| SEVERITY_LOW \|  \|<br>\| SEVERITY_CRITICAL \|  \| |
| `Source` | [`Source?`](../../doc/models/source.md) | Optional | Source of the Rule<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SOURCE_PRO \| From Pro rules \|<br>\| SOURCE_COMMUNITY \| From Semgrep Community rules \|<br>\| SOURCE_CUSTOM \| From Custom rules \| |
| `Technologies` | `List<string>` | Optional | Technologies the Rule is associated with. |
| `Url` | `string` | Optional | The URL of the Rule. |
| `VulnerabilityClass` | `List<string>` | Optional | Vulnerability classes the Rule is associated with. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Rule rule = new Rule
{
    Category = "security",
    Confidence = Confidence.ConfidenceHigh,
    CweCategories = new List<string>
    {
        "CWE-918: Server-Side Request Forgery (SSRF)",
    },
    HasValidators = false,
    Id = "id0",
    Languages = new List<string>
    {
        "python",
    },
    LastChangeAt = DateTime.ParseExact("2024-07-29 22:33:37.380293+00:00", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    OwaspCategories = new List<string>
    {
        "A07: Cross-Site Scripting (XSS)",
    },
    Path = "python.rule.1",
    PolicyMode = PolicyMode.ModeBlock,
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
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

