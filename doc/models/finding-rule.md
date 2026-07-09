
# Finding Rule

Rule that applies to this finding

*This model accepts additional fields of type object.*

## Structure

`FindingRule`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Category` | `string` | Optional | Category the rule is associated with |
| `Confidence` | [`Confidence2?`](../../doc/models/confidence-2.md) | Optional | Confidence level of the rule |
| `CweNames` | `List<string>` | Optional | CWE names associated with the rule |
| `Message` | `string` | Optional | Rule message |
| `Name` | `string` | Optional | Name of the rule |
| `OwaspNames` | `List<string>` | Optional | OWASP names associated with the rule |
| `Subcategories` | `List<string>` | Optional | Subcategories of the rule |
| `VulnerabilityClasses` | `List<string>` | Optional | Vulnerability classes the rule is associated with |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

FindingRule findingRule = new FindingRule
{
    Category = "security",
    Confidence = Confidence2.High,
    CweNames = new List<string>
    {
        "CWE-319: Cleartext Transmission of Sensitive Information",
    },
    Message = "This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.",
    Name = "html.security.plaintext-http-link.plaintext-http-link",
    OwaspNames = new List<string>
    {
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
    },
    Subcategories = new List<string>
    {
        "vuln",
    },
    VulnerabilityClasses = new List<string>
    {
        "Mishandled Sensitive Information",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

