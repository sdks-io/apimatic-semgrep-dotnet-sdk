
# Protos Openapi V1 List Deployments Response

*This model accepts additional fields of type object.*

## Structure

`ProtosOpenapiV1ListDeploymentsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Deployments` | [`List<Deployment>`](../../doc/models/deployment.md) | Optional | Return the deployment the supplied token can access. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;
using System.Collections.Generic;

ProtosOpenapiV1ListDeploymentsResponse protosOpenapiV1ListDeploymentsResponse = new ProtosOpenapiV1ListDeploymentsResponse
{
    Deployments = new List<Deployment>
    {
        new Deployment
        {
            Id = 106L,
            Name = "name6",
            Slug = "slug0",
            Findings = new EndpointReference
            {
                Url = "url2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Deployment
        {
            Id = 106L,
            Name = "name6",
            Slug = "slug0",
            Findings = new EndpointReference
            {
                Url = "url2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

