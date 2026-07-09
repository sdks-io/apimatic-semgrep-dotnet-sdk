# Scans Service

View details of scans associated with projects in your organization.

```csharp
ScansServiceApi scansServiceApi = client.ScansServiceApi;
```

## Class Name

`ScansServiceApi`

## Methods

* [Get Scan](../../doc/controllers/scans-service.md#get-scan)
* [Search Scans](../../doc/controllers/scans-service.md#search-scans)


# Get Scan

Request the details of a scan including the associated deployment, repository, and commit information.

```csharp
GetScanAsync(
    string deploymentId,
    string scanId)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `scanId` | `string` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1GetScanResponse](../../doc/models/protos-openapi-v1-get-scan-response.md).

## Example Usage

```csharp
string deploymentId = "123";
string scanId = "456";
try
{
    ApiResponse<ProtosOpenapiV1GetScanResponse> result = await scansServiceApi.GetScanAsync(
        deploymentId,
        scanId
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Search Scans

List the scans associated with a particular repository over the past 30 days.

```csharp
SearchScansAsync(
    string deploymentId,
    Models.SearchScansRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`SearchScansRequest`](../../doc/models/search-scans-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1SearchScansResponse](../../doc/models/protos-openapi-v1-search-scans-response.md).

## Example Usage

```csharp
string deploymentId = "123";
SearchScansRequest body = new SearchScansRequest
{
    DeploymentId = "123",
};

try
{
    ApiResponse<ProtosOpenapiV1SearchScansResponse> result = await scansServiceApi.SearchScansAsync(
        deploymentId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

