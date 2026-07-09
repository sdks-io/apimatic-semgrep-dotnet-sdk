
# Endpoint Reference

*This model accepts additional fields of type object.*

## Structure

`EndpointReference`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Url` | `string` | Required | URL that the reference is pointing to. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

EndpointReference endpointReference = new EndpointReference
{
    Url = "https://semgrep.dev/api/v1/deployments/123/findings",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

