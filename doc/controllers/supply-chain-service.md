# Supply Chain Service

Manage the Supply Chain findings and dependencies of your organization.

A request body is required, but may be an empty object.

```csharp
SupplyChainServiceApi supplyChainServiceApi = client.SupplyChainServiceApi;
```

## Class Name

`SupplyChainServiceApi`

## Methods

* [List Dependencies](../../doc/controllers/supply-chain-service.md#list-dependencies)
* [List Repositories for Dependencies](../../doc/controllers/supply-chain-service.md#list-repositories-for-dependencies)
* [List Lockfiles for Dependencies](../../doc/controllers/supply-chain-service.md#list-lockfiles-for-dependencies)
* [Create Sbom Export](../../doc/controllers/supply-chain-service.md#create-sbom-export)
* [Get Sbom Export](../../doc/controllers/supply-chain-service.md#get-sbom-export)


# List Dependencies

```csharp
ListDependenciesAsync(
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
    ApiResponse<ListDependenciesResponse> result = await supplyChainServiceApi.ListDependenciesAsync(
        deploymentId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# List Repositories for Dependencies

```csharp
ListRepositoriesForDependenciesAsync(
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
    ApiResponse<ListRepositoriesForDependenciesResponse> result = await supplyChainServiceApi.ListRepositoriesForDependenciesAsync(
        deploymentId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# List Lockfiles for Dependencies

```csharp
ListLockfilesForDependenciesAsync(
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
    ApiResponse<ListLockfilesForDependenciesResponse> result = await supplyChainServiceApi.ListLockfilesForDependenciesAsync(
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


# Create Sbom Export

```csharp
CreateSbomExportAsync(
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
    ApiResponse<CreateSbomExportResponse> result = await supplyChainServiceApi.CreateSbomExportAsync(
        deploymentId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Get Sbom Export

```csharp
GetSbomExportAsync(
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
    ApiResponse<GetSbomExportResponse> result = await supplyChainServiceApi.GetSbomExportAsync(
        deploymentId,
        taskToken
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

