# Deployments Service

Deployments encapsulate your organization's security organization, with multiple projects, policies, and integrations. As the root object of the organization, they're similarly the root object of the API.

```csharp
DeploymentsServiceApi deploymentsServiceApi = client.DeploymentsServiceApi;
```

## Class Name

`DeploymentsServiceApi`


# Deployments Service List Deployments

Request the deployments your auth can access.

Currently available auth scope does not extend over more than one deployment. This endpoint returns the single deployment your token can access. The endpoint additionally returns links to related resources available on this API.

```csharp
DeploymentsServiceListDeploymentsAsync()
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1ListDeploymentsResponse](../../doc/models/protos-openapi-v1-list-deployments-response.md).

## Example Usage

```csharp
try
{
    ApiResponse<ProtosOpenapiV1ListDeploymentsResponse> result = await deploymentsServiceApi.DeploymentsServiceListDeploymentsAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

