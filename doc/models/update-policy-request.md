
# Update Policy Request

*This model accepts additional fields of type object.*

## Structure

`UpdatePolicyRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `PolicyId` | `string` | Required | Policy ID (numeric). Example: `456`. Can be found at `/deployments/{deploymentId}/policies`. |
| `PolicyMode` | [`PolicyMode3`](../../doc/models/policy-mode-3.md) | Required | New policy mode to set for the Rule.<br><br>- MODE_MONITOR: Monitor mode, silently report findings<br>- MODE_COMMENT: Comment mode, leaves PR comments but does not block<br>- MODE_BLOCK: Block mode, leaves PR comments and blocks PR<br>- MODE_DISABLED: Disabled mode, not active<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| MODE_MONITOR \| Monitor mode, silently report findings \|<br>\| MODE_COMMENT \| Comment mode, leaves PR comments but does not block \|<br>\| MODE_BLOCK \| Block mode, leaves PR comments and blocks PR \|<br>\| MODE_DISABLED \| Disabled mode, not active \| |
| `RulePath` | `string` | Required | Full path of the Rule. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example

```csharp
using SemgrepWebApp.Standard.Models;
using SemgrepWebApp.Standard.Utilities;

UpdatePolicyRequest updatePolicyRequest = new UpdatePolicyRequest
{
    DeploymentId = "123",
    PolicyId = "456",
    PolicyMode = PolicyMode3.ModeMonitor,
    RulePath = "rulePath2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```

