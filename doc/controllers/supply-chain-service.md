# Supply Chain Service

Manage the Supply Chain findings and dependencies of your organization.

A request body is required, but may be an empty object.

```csharp
SupplyChainServiceApi supplyChainServiceApi = client.SupplyChainServiceApi;
```

## Class Name

`SupplyChainServiceApi`

## Methods

* [Supply Chain Service List Dependencies](../../doc/controllers/supply-chain-service.md#supply-chain-service-list-dependencies)
* [Supply Chain Service List Repositories for Dependencies](../../doc/controllers/supply-chain-service.md#supply-chain-service-list-repositories-for-dependencies)
* [Supply Chain Service List Lockfiles for Dependencies](../../doc/controllers/supply-chain-service.md#supply-chain-service-list-lockfiles-for-dependencies)
* [Supply Chain Service Create Sbom Export](../../doc/controllers/supply-chain-service.md#supply-chain-service-create-sbom-export)
* [Supply Chain Service Get Sbom Export](../../doc/controllers/supply-chain-service.md#supply-chain-service-get-sbom-export)


# Supply Chain Service List Dependencies

```csharp
SupplyChainServiceListDependenciesAsync(
    string deploymentId,
    Models.ListDependenciesRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`ListDependenciesRequest`](../../doc/models/list-dependencies-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ListDependenciesResponse](../../doc/models/list-dependencies-response.md).

## Example Usage

```csharp
string deploymentId = "123";
ListDependenciesRequest body = new ListDependenciesRequest
{
    DeploymentId = "123",
    PageSize = 1000L,
};

try
{
    ApiResponse<ListDependenciesResponse> result = await supplyChainServiceApi.SupplyChainServiceListDependenciesAsync(
        deploymentId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Supply Chain Service List Repositories for Dependencies

```csharp
SupplyChainServiceListRepositoriesForDependenciesAsync(
    string deploymentId,
    Models.ListRepositoriesForDependenciesRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`ListRepositoriesForDependenciesRequest`](../../doc/models/list-repositories-for-dependencies-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ListRepositoriesForDependenciesResponse](../../doc/models/list-repositories-for-dependencies-response.md).

## Example Usage

```csharp
string deploymentId = "deploymentId2";
ListRepositoriesForDependenciesRequest body = new ListRepositoriesForDependenciesRequest
{
    DeploymentId = "deploymentId8",
    PageSize = 100L,
};

try
{
    ApiResponse<ListRepositoriesForDependenciesResponse> result = await supplyChainServiceApi.SupplyChainServiceListRepositoriesForDependenciesAsync(
        deploymentId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Supply Chain Service List Lockfiles for Dependencies

```csharp
SupplyChainServiceListLockfilesForDependenciesAsync(
    string deploymentId,
    string repositoryId,
    Models.ListLockfilesForDependenciesRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `repositoryId` | `string` | Template, Required | - |
| `body` | [`ListLockfilesForDependenciesRequest`](../../doc/models/list-lockfiles-for-dependencies-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ListLockfilesForDependenciesResponse](../../doc/models/list-lockfiles-for-dependencies-response.md).

## Example Usage

```csharp
string deploymentId = "deploymentId2";
string repositoryId = "repositoryId6";
ListLockfilesForDependenciesRequest body = new ListLockfilesForDependenciesRequest
{
    DeploymentId = "deploymentId8",
    RepositoryId = "repositoryId0",
    PageSize = 100L,
};

try
{
    ApiResponse<ListLockfilesForDependenciesResponse> result = await supplyChainServiceApi.SupplyChainServiceListLockfilesForDependenciesAsync(
        deploymentId,
        repositoryId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Supply Chain Service Create Sbom Export

```csharp
SupplyChainServiceCreateSbomExportAsync(
    string deploymentId,
    Models.CreateSbomExportRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`CreateSbomExportRequest`](../../doc/models/create-sbom-export-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.CreateSbomExportResponse](../../doc/models/create-sbom-export-response.md).

## Example Usage

```csharp
string deploymentId = "123";
CreateSbomExportRequest body = new CreateSbomExportRequest
{
    DeploymentId = "123",
    MetadataComponentType = MetadataComponentType.SbomMetadataComponentTypeCycloneDxV15Application,
    MRef = "refs/pull/1234/merge",
    RepositoryId = "123",
    SbomOutputFormat = SbomOutputFormat.SbomOutputFormatJson,
};

try
{
    ApiResponse<CreateSbomExportResponse> result = await supplyChainServiceApi.SupplyChainServiceCreateSbomExportAsync(
        deploymentId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Supply Chain Service Get Sbom Export

```csharp
SupplyChainServiceGetSbomExportAsync(
    string deploymentId,
    string taskToken)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `taskToken` | `string` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.GetSbomExportResponse](../../doc/models/get-sbom-export-response.md).

## Example Usage

```csharp
string deploymentId = "123";
string taskToken = "taskToken2";
try
{
    ApiResponse<GetSbomExportResponse> result = await supplyChainServiceApi.SupplyChainServiceGetSbomExportAsync(
        deploymentId,
        taskToken
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

