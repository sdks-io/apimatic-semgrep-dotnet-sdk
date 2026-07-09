
# Rule Explanation

AI-generated explanation of why a rule flagged this specific code

*This model accepts additional fields of type object.*

## Structure

`RuleExplanation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Explanation` | `string` | Optional | Detailed explanation of why this rule flagged the code, including context about the security issue and why it applies to this specific code. AI generated content, review carefully |
| `Summary` | `string` | Optional | A concise summary of the rule explanation. May not be present for all findings |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

RuleExplanation ruleExplanation = new RuleExplanation
{
    Explanation = "This code is vulnerable to SQL injection because user input from the `username` parameter is directly concatenated into the SQL query string without sanitization or parameterization.",
    Summary = "User input directly concatenated into SQL query",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

