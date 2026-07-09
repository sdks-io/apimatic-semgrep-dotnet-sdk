# Policies Service

View and manage the Policies of your organization.

```csharp
PoliciesServiceApi policiesServiceApi = client.PoliciesServiceApi;
```

## Class Name

`PoliciesServiceApi`

## Methods

* [List Policies](../../doc/controllers/policies-service.md#list-policies)
* [List Policy Rules](../../doc/controllers/policies-service.md#list-policy-rules)
* [Update Policy](../../doc/controllers/policies-service.md#update-policy)


# List Policies

```csharp
ListPoliciesAsync(
    string deploymentId)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1ListPoliciesResponse](../../doc/models/protos-openapi-v1-list-policies-response.md).

## Example Usage

```csharp
string deploymentId = "123";
try
{
    ApiResponse<ProtosOpenapiV1ListPoliciesResponse> result = await policiesServiceApi.ListPoliciesAsync(deploymentId);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# List Policy Rules

```csharp
ListPolicyRulesAsync(
    string deploymentId,
    string policyId,
    string cursor = null,
    long? limit = null)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `policyId` | `string` | Template, Required | - |
| `cursor` | `string` | Query, Optional | - |
| `limit` | `long?` | Query, Optional | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1ListPolicyRulesResponse](../../doc/models/protos-openapi-v1-list-policy-rules-response.md).

## Example Usage

```csharp
string deploymentId = "123";
string policyId = "456";
try
{
    ApiResponse<ProtosOpenapiV1ListPolicyRulesResponse> result = await policiesServiceApi.ListPolicyRulesAsync(
        deploymentId,
        policyId
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Update Policy

```csharp
UpdatePolicyAsync(
    string deploymentId,
    string policyId,
    Models.UpdatePolicyRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `policyId` | `string` | Template, Required | - |
| `body` | [`UpdatePolicyRequest`](../../doc/models/update-policy-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1UpdatePolicyResponse](../../doc/models/protos-openapi-v1-update-policy-response.md).

## Example Usage

```csharp
string deploymentId = "123";
string policyId = "456";
UpdatePolicyRequest body = new UpdatePolicyRequest
{
    DeploymentId = "123",
    PolicyId = "456",
    PolicyMode = PolicyMode3.ModeBlock,
    RulePath = "rulePath2",
};

try
{
    ApiResponse<ProtosOpenapiV1UpdatePolicyResponse> result = await policiesServiceApi.UpdatePolicyAsync(
        deploymentId,
        policyId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

