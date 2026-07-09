
# Protos Openapi V1 Get Bootstrap Sms Vpc Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1GetBootstrapSmsVpcResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AwsTemplateFormatVersion` | `string` | Optional | The AWSTemplateFormatVersion that the template conforms to |
| `Description` | `string` | Optional | Template description |
| `Metadata` | `object` | Optional | Template metadata including version and last updated date |
| `Outputs` | `object` | Optional | Output values of the stack |
| `Parameters` | `object` | Optional | Template parameters |
| `Resources` | `object` | Optional | Declaration of AWS resources |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ProtosOpenapiV1GetBootstrapSmsVpcResponse protosOpenapiV1GetBootstrapSmsVpcResponse = new ProtosOpenapiV1GetBootstrapSmsVpcResponse
{
    AwsTemplateFormatVersion = "AWSTemplateFormatVersion0",
    Description = "Description8",
    Metadata = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    Outputs = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    Parameters = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

