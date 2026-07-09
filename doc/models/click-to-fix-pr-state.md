
# Click to Fix Pr State

Filter findings by Click-to-Fix PR state. If not specified, returns all findings regardless of autofix PR status. This filter applies to both sast and sca issue types. Valid values: open, merged

## Enumeration

`ClickToFixPrState`

## Fields

| Name |
|  --- |
| `Open` |
| `Merged` |

## Example

```csharp
using SemgrepWebApp.Standard.Models;

ClickToFixPrState clickToFixPrState = ClickToFixPrState.Open;
```

