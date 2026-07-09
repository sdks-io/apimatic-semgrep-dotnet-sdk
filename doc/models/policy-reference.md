
# Policy Reference

Reference to a policy, with some basic information. If null, then the information does not exist or lacks integrity (older or broken scans)

*This model accepts additional fields of type object.*

## Structure

`PolicyReference`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `long?` | Optional | Unique numerical identifier of the policy |
| `Name` | `string` | Optional | Human readable name |
| `Slug` | `string` | Optional | Sanitized machine-readable name |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

PolicyReference policyReference = new PolicyReference
{
    Id = 120L,
    Name = "Default Policy",
    Slug = "default-policy",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

