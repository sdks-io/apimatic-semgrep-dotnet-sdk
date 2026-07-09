
# Product Type

Product type the Policy applies to.

| value | description |
|-------|---------------|
| PRODUCT_TYPE_SAST | The product type for Code rules. |
| PRODUCT_TYPE_SECRETS | The product type for Secrets rules. |

## Enumeration

`ProductType`

## Fields

| Name |
|  --- |
| `ProductTypeSast` |
| `ProductTypeSecrets` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

ProductType productType = ProductType.ProductTypeSast;
```

