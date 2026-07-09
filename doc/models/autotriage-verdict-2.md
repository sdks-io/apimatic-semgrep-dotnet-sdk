
# Autotriage Verdict 2

Which autotriage verdict do you want to include? If not specified, includes all. This filter is applicable when `issue_type` is `sast` or unspecified. Valid values: true_positive, false_positive

## Enumeration

`AutotriageVerdict2`

## Fields

| Name |
|  --- |
| `TruePositive` |
| `FalsePositive` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

AutotriageVerdict2 autotriageVerdict2 = AutotriageVerdict2.TruePositive;
```

