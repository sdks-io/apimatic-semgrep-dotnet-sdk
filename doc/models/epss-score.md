
# Epss Score

The score assigned by FIRST.org's Exploitation Probability Scoring System

*This model accepts additional fields of type object.*

## Structure

`EpssScore`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Percentile` | `double?` | Optional | This EPSS score's percentile among all EPSS scores, from 0 to 1 |
| `Score` | `double?` | Optional | The explotation probability, from 0 to 1 |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

EpssScore epssScore = new EpssScore
{
    Percentile = 0.994,
    Score = 0.97,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

