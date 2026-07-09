
# Search Scans Request

*This model accepts additional fields of type object.*

## Structure

`SearchScansRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Branch` | `string` | Optional | Only get scans from the specified branch |
| `Cursor` | `string` | Optional | Cursor to paginate through the results |
| `DeploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `IsFullScan` | `int?` | Optional | Only get scans that are full scans (if false, only get diff scans) |
| `Limit` | `int?` | Optional | Page size to paginate through the results (default is 100, max is 500) |
| `Products` | [`Products?`](../../doc/models/products.md) | Optional | Only get scans that have these enabled products<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| PRODUCT_SAST \|  \|<br>\| PRODUCT_SCA \|  \|<br>\| PRODUCT_SECRETS \|  \|<br>\| PRODUCT_AI_SAST \|  \| |
| `RepositoryId` | `int?` | Optional | Only get scans for this repo |
| `Since` | `DateTime?` | Optional | Only get scans created after this time. Provide time in ISO 8601 format. |
| `Statuses` | [`Statuses?`](../../doc/models/statuses.md) | Optional | Only get scans that have one of these statuses<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SCAN_STATUS_RUNNING \| The scan is currently running \|<br>\| SCAN_STATUS_COMPLETED \| The scan has completed successfully (0 or 1 exit code) \|<br>\| SCAN_STATUS_PENDING \| The scan is queued and waiting to start \|<br>\| SCAN_STATUS_CANCELLED \| The scan was cancelled before completion \|<br>\| SCAN_STATUS_ERROR \| The scan has exited with a failure (exit code not 0 or 1) \|<br>\| SCAN_STATUS_NEVER_FINISHED \| The scan did not report an error or success after over an hour \| |
| `TotalTime` | [`FloatRange`](../../doc/models/float-range.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

SearchScansRequest searchScansRequest = new SearchScansRequest
{
    DeploymentId = "123",
    Branch = "branch6",
    Cursor = "cursor6",
    IsFullScan = 26,
    Limit = 236,
    Products = Products.ProductSast,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

