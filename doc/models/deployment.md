
# Deployment

Deployment record, with relevant meta-data and further accesses.

*This model accepts additional fields of type object.*

## Structure

`Deployment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Findings` | [`EndpointReference`](../../doc/models/endpoint-reference.md) | Optional | - |
| `Id` | `long` | Required | Unique numerical identifier of the deployment. |
| `Name` | `string` | Required | Human readable name. |
| `Slug` | `string` | Required | Sanitized machine-readable name. Used as primary identifier through the web API. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

Deployment deployment = new Deployment
{
    Id = 120L,
    Name = "Your Deployment",
    Slug = "your-deployment",
    Findings = new EndpointReference
    {
        Url = "url2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

