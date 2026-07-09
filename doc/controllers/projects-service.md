# Projects Service

```csharp
ProjectsServiceApi projectsServiceApi = client.ProjectsServiceApi;
```

## Class Name

`ProjectsServiceApi`

## Methods

* [List Projects](../../doc/controllers/projects-service.md#list-projects)
* [Delete Project](../../doc/controllers/projects-service.md#delete-project)
* [Get Project](../../doc/controllers/projects-service.md#get-project)
* [Update Project](../../doc/controllers/projects-service.md#update-project)
* [Toggle Project Managed Scan](../../doc/controllers/projects-service.md#toggle-project-managed-scan)
* [Delete Project Tags](../../doc/controllers/projects-service.md#delete-project-tags)
* [Add Project Tags](../../doc/controllers/projects-service.md#add-project-tags)


# List Projects

Request the list of projects that have been scanned or onboarded to Managed Scans. Does not return archived repositories. Returns 100 projects per page by default.

```csharp
ListProjectsAsync(
    string deploymentSlug,
    long? page = null,
    long? pageSize = 100L)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `page` | `long?` | Query, Optional | - |
| `pageSize` | `long?` | Query, Optional | **Default**: `100L` |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ListProjectsResponse](../../doc/models/list-projects-response.md).

## Example Usage

```csharp
string deploymentSlug = "your-deployment";
long? page = 1L;
long? pageSize = 100L;
try
{
    ApiResponse<ListProjectsResponse> result = await projectsServiceApi.ListProjectsAsync(
        deploymentSlug,
        page,
        pageSize
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Delete Project

Delete a project for a deployment you have access to. This will also delete all of the associated findings.

```csharp
DeleteProjectAsync(
    string deploymentSlug,
    string projectName)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.DeleteProjectResponse](../../doc/models/delete-project-response.md).

## Example Usage

```csharp
string deploymentSlug = "your-deployment";
string projectName = "organization/project";
try
{
    ApiResponse<DeleteProjectResponse> result = await projectsServiceApi.DeleteProjectAsync(
        deploymentSlug,
        projectName
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Get Project

Retrieve details for a single project associated with a deployment that you have access to.

```csharp
GetProjectAsync(
    string deploymentSlug,
    string projectName)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.GetProjectResponse](../../doc/models/get-project-response.md).

## Example Usage

```csharp
string deploymentSlug = "your-deployment";
string projectName = "organization/project";
try
{
    ApiResponse<GetProjectResponse> result = await projectsServiceApi.GetProjectAsync(
        deploymentSlug,
        projectName
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Update Project

Update attributes for the project using the value passed in to the request body.

Note: The only attribute that is supported as of January 2023 is `tags`.

```csharp
UpdateProjectAsync(
    string deploymentSlug,
    string projectName,
    Models.UpdateProjectRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `body` | [`UpdateProjectRequest`](../../doc/models/update-project-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.UpdateProjectResponse](../../doc/models/update-project-response.md).

## Example Usage

```csharp
string deploymentSlug = "your-deployment";
string projectName = "organization/project";
UpdateProjectRequest body = new UpdateProjectRequest
{
    DeploymentSlug = "your-deployment",
    ProjectName = "organization/project",
    PrimaryBranch = "refs/heads/develop",
    Tags = new List<string>
    {
        "tag",
    },
};

try
{
    ApiResponse<UpdateProjectResponse> result = await projectsServiceApi.UpdateProjectAsync(
        deploymentSlug,
        projectName,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Toggle Project Managed Scan

Enable or disable
[Semgrep Managed Scans](/docs/deployment/managed-scanning/overview)
for a project.

```csharp
ToggleProjectManagedScanAsync(
    string deploymentSlug,
    string projectName,
    Models.ToggleProjectManagedScanRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `body` | [`ToggleProjectManagedScanRequest`](../../doc/models/toggle-project-managed-scan-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ToggleProjectManagedScanResponse](../../doc/models/toggle-project-managed-scan-response.md).

## Example Usage

```csharp
string deploymentSlug = "your-deployment";
string projectName = "organization/project";
ToggleProjectManagedScanRequest body = new ToggleProjectManagedScanRequest
{
    DeploymentSlug = "your-deployment",
    ProjectName = "organization/project",
};

try
{
    ApiResponse<ToggleProjectManagedScanResponse> result = await projectsServiceApi.ToggleProjectManagedScanAsync(
        deploymentSlug,
        projectName,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Delete Project Tags

Remove tags from a project for a deployment you have access to.

This request will not delete project tags from the deployment and will only remove
them from the requested project. Any other projects associated with the requested
tag will remain unaffected.

```csharp
DeleteProjectTagsAsync(
    string deploymentSlug,
    string projectName,
    List<string> tags = null)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `tags` | `List<string>` | Query, Optional | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.DeleteProjectTagsResponse](../../doc/models/delete-project-tags-response.md).

## Example Usage

```csharp
string deploymentSlug = "your-deployment";
string projectName = "organization/project";
List<string> tags = new List<string>
{
    "tag",
};

try
{
    ApiResponse<DeleteProjectTagsResponse> result = await projectsServiceApi.DeleteProjectTagsAsync(
        deploymentSlug,
        projectName,
        tags
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Add Project Tags

Add tags to a project for a deployment you have access to.

Any project tags that do not already exist for the deployment will be created automatically and associated with the project.

```csharp
AddProjectTagsAsync(
    string deploymentSlug,
    string projectName,
    Models.AddProjectTagsRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `body` | [`AddProjectTagsRequest`](../../doc/models/add-project-tags-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.AddProjectTagsResponse](../../doc/models/add-project-tags-response.md).

## Example Usage

```csharp
string deploymentSlug = "your-deployment";
string projectName = "organization/project";
AddProjectTagsRequest body = new AddProjectTagsRequest
{
    DeploymentSlug = "your-deployment",
    ProjectName = "organization/project",
    Tags = new List<string>
    {
        "tag",
    },
};

try
{
    ApiResponse<AddProjectTagsResponse> result = await projectsServiceApi.AddProjectTagsAsync(
        deploymentSlug,
        projectName,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

