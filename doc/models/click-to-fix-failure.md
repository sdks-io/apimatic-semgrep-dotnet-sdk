
# Click to Fix Failure

A failed PR creation attempt by Semgrep's Click to Fix feature

*This model accepts additional fields of type object.*

## Structure

`ClickToFixFailure`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `string` | Optional | When this failure occurred |
| `Reason` | `string` | Optional | Reason for the PR creation failure |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

ClickToFixFailure clickToFixFailure = new ClickToFixFailure
{
    CreatedAt = "2024-01-15 10:30:00+00:00",
    Reason = "merge conflict in target branch",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

