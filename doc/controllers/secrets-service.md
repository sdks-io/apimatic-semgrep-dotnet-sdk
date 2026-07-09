# Secrets Service

View and manage the Secrets of your organization.

```csharp
SecretsServiceApi secretsServiceApi = client.SecretsServiceApi;
```

## Class Name

`SecretsServiceApi`


# List Secrets Path

```csharp
ListSecretsPathAsync(
    string deploymentId,
    string cursor = null,
    long? limit = null,
    DateTime? since = null,
    List<Models.ValidationState3> validationState = null,
    Models.Status8? status = Models.Status8.FindingStatusUnspecified,
    List<Models.Severity5> severity = null,
    List<string> repo = null)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `cursor` | `string` | Query, Optional | - |
| `limit` | `long?` | Query, Optional | - |
| `since` | `DateTime?` | Query, Optional | - |
| `validationState` | [`List<ValidationState3>`](../../doc/models/validation-state-3.md) | Query, Optional | - |
| `status` | [`Status8?`](../../doc/models/status-8.md) | Query, Optional | **Default**: `Status8.FINDING_STATUS_UNSPECIFIED` |
| `severity` | [`List<Severity5>`](../../doc/models/severity-5.md) | Query, Optional | - |
| `repo` | `List<string>` | Query, Optional | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1ListSecretsPathResponse](../../doc/models/protos-openapi-v1-list-secrets-path-response.md).

## Example Usage

```csharp
string deploymentId = "123";
Status8? status = Status8.FindingStatusUnspecified;
try
{
    ApiResponse<ProtosOpenapiV1ListSecretsPathResponse> result = await secretsServiceApi.ListSecretsPathAsync(
        deploymentId,
        null,
        null,
        null,
        null,
        status
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

