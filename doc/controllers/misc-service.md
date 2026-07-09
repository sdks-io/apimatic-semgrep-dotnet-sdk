# Misc Service

Utility endpoints.

```csharp
MiscServiceApi miscServiceApi = client.MiscServiceApi;
```

## Class Name

`MiscServiceApi`

## Methods

* [Misc Service Get Bootstrap Sms Vpc](../../doc/controllers/misc-service.md#misc-service-get-bootstrap-sms-vpc)
* [Misc Service Ping](../../doc/controllers/misc-service.md#misc-service-ping)


# Misc Service Get Bootstrap Sms Vpc

VPC support for Managed Scans is in private beta.

Returns the Managed Scans VPC Bootstrap CloudFormation template in JSON format for setting up cross-account infrastructure.

This template creates IAM roles and policies needed for Semgrep Managed Scanning (SMS) VPC infrastructure automation,
including the semgrep-sms-vpc-automation role and EC2 Image Builder distribution roles for gVisor container runtime.

See the original AWS cloudformation template format at https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-formats.html

:information_source: **Note** This endpoint does not require authentication.

```csharp
MiscServiceGetBootstrapSmsVpcAsync()
```

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1GetBootstrapSmsVpcResponse](../../doc/models/protos-openapi-v1-get-bootstrap-sms-vpc-response.md).

## Example Usage

```csharp
try
{
    ApiResponse<ProtosOpenapiV1GetBootstrapSmsVpcResponse> result = await miscServiceApi.MiscServiceGetBootstrapSmsVpcAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Misc Service Ping

Use to ping the server and assert liveness.

:information_source: **Note** This endpoint does not require authentication.

```csharp
MiscServicePingAsync()
```

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type object.

## Example Usage

```csharp
try
{
    ApiResponse<object> result = await miscServiceApi.MiscServicePingAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

