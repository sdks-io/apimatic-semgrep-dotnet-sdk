
# Protos Openapi V1 List Policies Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1ListPoliciesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Policies` | [`List<Policy>`](../../doc/models/policy.md) | Optional | List of Policies associated with the given Deployment. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1ListPoliciesResponse protosOpenapiV1ListPoliciesResponse = new ProtosOpenapiV1ListPoliciesResponse
{
    Policies = new List<Policy>
    {
        new Policy
        {
            Id = "1",
            IsDefault = true,
            Name = "Global Policy",
            ProductType = ProductType.ProductTypeSast,
            Slug = "global_policy",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Policy
        {
            Id = "2",
            IsDefault = false,
            Name = "Semgrep test",
            ProductType = ProductType.ProductTypeSast,
            Slug = "semgrep_test",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Policy
        {
            Id = "3",
            IsDefault = true,
            Name = "Global Secrets Policy",
            ProductType = ProductType.ProductTypeSecrets,
            Slug = "global_secrets_policy",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

