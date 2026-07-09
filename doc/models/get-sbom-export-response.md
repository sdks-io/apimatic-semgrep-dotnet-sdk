
# Get Sbom Export Response

*This model accepts additional fields of type object.*

## Structure

`GetSbomExportResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DownloadUrl` | `string` | Optional | URL to download the SBOM when status is COMPLETED. |
| `ErrorMessage` | `string` | Optional | Error message when status is FAILED. |
| `Status` | [`Status3`](../../doc/models/status-3.md) | Required | Status of the SBOM export job.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_EXPORT_STATUS_IN_PROGRESS \| The SBOM export job is in progress. \|<br>\| SBOM_EXPORT_STATUS_COMPLETED \| The SBOM export job has completed. \|<br>\| SBOM_EXPORT_STATUS_FAILED \| The SBOM export job has failed. \| |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

GetSbomExportResponse getSbomExportResponse = new GetSbomExportResponse
{
    Status = Status3.SbomExportStatusCompleted,
    DownloadUrl = "downloadUrl6",
    ErrorMessage = "errorMessage2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

