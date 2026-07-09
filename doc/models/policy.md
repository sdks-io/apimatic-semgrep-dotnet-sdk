
# Policy

*This model accepts additional fields of type object.*

## Structure

`Policy`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | ID of the Policy. |
| `IsDefault` | `bool?` | Optional | When True, the Policy applies to all repositories. |
| `Name` | `string` | Optional | Name of the Policy. |
| `ProductType` | [`ProductType?`](../../doc/models/product-type.md) | Optional | Product type the Policy applies to.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| PRODUCT_TYPE_SAST \| The product type for Code rules. \|<br>\| PRODUCT_TYPE_SECRETS \| The product type for Secrets rules. \| |
| `Slug` | `string` | Optional | Sanitized machine-readable name of the Policy. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

Policy policy = new Policy
{
    Id = "1",
    IsDefault = true,
    Name = "Global Policy",
    ProductType = ProductType.ProductTypeSast,
    Slug = "global_policy",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

