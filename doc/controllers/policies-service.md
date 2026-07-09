# Policies Service

View and manage the Policies of your organization.

```csharp
PoliciesServiceApi policiesServiceApi = client.PoliciesServiceApi;
```

## Class Name

`PoliciesServiceApi`

## Methods

* [Policies Service List Policies](../../doc/controllers/policies-service.md#policies-service-list-policies)
* [Policies Service List Policy Rules](../../doc/controllers/policies-service.md#policies-service-list-policy-rules)
* [Policies Service Update Policy](../../doc/controllers/policies-service.md#policies-service-update-policy)


# Policies Service List Policies

```csharp
PoliciesServiceListPoliciesAsync(
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
    ApiResponse<ProtosOpenapiV1ListPoliciesResponse> result = await policiesServiceApi.PoliciesServiceListPoliciesAsync(deploymentId);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Policies Service List Policy Rules

```csharp
PoliciesServiceListPolicyRulesAsync(
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
    ApiResponse<ProtosOpenapiV1ListPolicyRulesResponse> result = await policiesServiceApi.PoliciesServiceListPolicyRulesAsync(
        deploymentId,
        policyId
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Policies Service Update Policy

```csharp
PoliciesServiceUpdatePolicyAsync(
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
    ApiResponse<ProtosOpenapiV1UpdatePolicyResponse> result = await policiesServiceApi.PoliciesServiceUpdatePolicyAsync(
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

