
# Protos Openapi V1 Update Policy Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1UpdatePolicyResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PolicyId` | `string` | Optional | Policy ID (numeric). Example: `456`. Can be found at `/deployments/{deploymentId}/policies`. |
| `UpdatedRule` | [`Rule`](../../doc/models/rule.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1UpdatePolicyResponse protosOpenapiV1UpdatePolicyResponse = new ProtosOpenapiV1UpdatePolicyResponse
{
    PolicyId = "1",
    UpdatedRule = new Rule
    {
        Category = "category4",
        Confidence = Confidence.ConfidenceHigh,
        CweCategories = new List<string>
        {
            "cweCategories9",
        },
        HasValidators = false,
        Id = "id6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

