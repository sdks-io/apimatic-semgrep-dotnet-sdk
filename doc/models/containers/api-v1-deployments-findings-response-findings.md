
# Api V1 Deployments Findings Response Findings

## Class Name

`ApiV1DeploymentsFindingsResponseFindings`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`SastFinding`](../../../doc/models/sast-finding.md) | ApiV1DeploymentsFindingsResponseFindings.FromSastFinding(SastFinding sastFinding) |
| [`ScaFinding`](../../../doc/models/sca-finding.md) | ApiV1DeploymentsFindingsResponseFindings.FromScaFinding(ScaFinding scaFinding) |
| [`AiPoweredScanFinding`](../../../doc/models/ai-powered-scan-finding.md) | ApiV1DeploymentsFindingsResponseFindings.FromAIPoweredScanFinding(AiPoweredScanFinding aiPoweredScanFinding) |

## SastFinding

### Initialization Code

#### Example

```csharp
ApiV1DeploymentsFindingsResponseFindings value = ApiV1DeploymentsFindingsResponseFindings.FromSastFinding(
    new SastFinding
    {
        Categories = new List<string>
        {
            "security",
        },
        Confidence = Confidence1.Medium,
        CreatedAt = "2020-11-18 23:28:12.391807+00:00",
        FirstSeenScanId = 1234L,
        Id = 1234567L,
        LineOfCodeUrl = "https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1",
        MatchBasedId = "0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1",
        MRef = "refs/pull/1234/merge",
        RelevantSince = "2020-11-18 23:28:12.391807+00:00",
        RuleName = "typescript.react.security.audit.react-no-refs.react-no-refs",
        Severity = Severity1.Medium,
        State = State.Unresolved,
        StateUpdatedAt = "2020-11-19 23:28:12.391807+00:00",
        Status = Status.Open,
        SyntacticId = "440eeface888e78afceac3dc7d4cc2cf",
        TriageComment = "This finding is from the test repo",
        TriageReason = TriageReason.AcceptableRisk,
        TriageState = TriageState.Untriaged,
        TriagedAt = "2020-11-19 23:28:12.391807+00:00",
    }
);
```

## ScaFinding

### Initialization Code

#### Example

```csharp
ApiV1DeploymentsFindingsResponseFindings value = ApiV1DeploymentsFindingsResponseFindings.FromScaFinding(
    new ScaFinding
    {
        Categories = new List<string>
        {
            "security",
        },
        Confidence = Confidence1.Medium,
        CreatedAt = "2020-11-18 23:28:12.391807+00:00",
        FirstSeenScanId = 1234L,
        Id = 1234567L,
        IsMalicious = true,
        LineOfCodeUrl = "https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1",
        MatchBasedId = "0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1",
        Reachability = Reachability.Reachable,
        ReachableCondition = "you use the package on a host running Linux or MacOS",
        MRef = "refs/pull/1234/merge",
        RelevantSince = "2020-11-18 23:28:12.391807+00:00",
        RuleName = "typescript.react.security.audit.react-no-refs.react-no-refs",
        Severity = Severity1.Medium,
        State = State.Unresolved,
        StateUpdatedAt = "2020-11-19 23:28:12.391807+00:00",
        Status = Status.Open,
        SyntacticId = "440eeface888e78afceac3dc7d4cc2cf",
        TriageComment = "This finding is from the test repo",
        TriageReason = TriageReason.AcceptableRisk,
        TriageState = TriageState.Untriaged,
        TriagedAt = "2020-11-19 23:28:12.391807+00:00",
        VulnerabilityIdentifier = "CVE-2021-24112",
    }
);
```

## AiPoweredScanFinding

### Initialization Code

#### Example

```csharp
ApiV1DeploymentsFindingsResponseFindings value = ApiV1DeploymentsFindingsResponseFindings.FromAIPoweredScanFinding(
    new AiPoweredScanFinding
    {
        AiImpact = "An attacker could access or modify other users' data by manipulating the resource identifier in the request",
        Confidence = Confidence1.Medium,
        CreatedAt = "2020-11-18 23:28:12.391807+00:00",
        FirstSeenScanId = 1234L,
        Id = 1234567L,
        LineOfCodeUrl = "https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1",
        MatchBasedId = "0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1",
        MRef = "refs/pull/1234/merge",
        RelevantSince = "2020-11-18 23:28:12.391807+00:00",
        RuleName = "ai.detection.idor",
        Severity = Severity1.High,
        State = State.Unresolved,
        StateUpdatedAt = "2020-11-19 23:28:12.391807+00:00",
        Status = Status.Open,
        SyntacticId = "440eeface888e78afceac3dc7d4cc2cf",
        TriageComment = "This finding is from the test repo",
        TriageReason = TriageReason.AcceptableRisk,
        TriageState = TriageState.Untriaged,
        TriagedAt = "2020-11-19 23:28:12.391807+00:00",
    }
);
```

