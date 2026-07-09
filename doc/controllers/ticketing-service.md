# Ticketing Service

Create and manage external tickets

```csharp
TicketingServiceApi ticketingServiceApi = client.TicketingServiceApi;
```

## Class Name

`TicketingServiceApi`

## Methods

* [Delete Ticket](../../doc/controllers/ticketing-service.md#delete-ticket)
* [Link Ticket](../../doc/controllers/ticketing-service.md#link-ticket)
* [Unlink Ticket](../../doc/controllers/ticketing-service.md#unlink-ticket)
* [Create Ticket](../../doc/controllers/ticketing-service.md#create-ticket)


# Delete Ticket

Unlink a Jira ticket by its ID

```csharp
DeleteTicketAsync(
    string deploymentId,
    long externalTicketId)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `externalTicketId` | `long` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1DeleteTicketResponse](../../doc/models/protos-openapi-v1-delete-ticket-response.md).

## Example Usage

```csharp
string deploymentId = "123";
long externalTicketId = 456L;
try
{
    ApiResponse<ProtosOpenapiV1DeleteTicketResponse> result = await ticketingServiceApi.DeleteTicketAsync(
        deploymentId,
        externalTicketId
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Link Ticket

Link an existing external ticket (e.g. Jira) to one or more Semgrep findings by providing the ticket URL and a list of finding IDs. This does not create a ticket in your issue tracker — it only records the association in Semgrep. If a finding is already linked to a different ticket, the existing link is replaced. Requires a configured ticketing integration.

```csharp
LinkTicketAsync(
    string deploymentId,
    Models.LinkTicketRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`LinkTicketRequest`](../../doc/models/link-ticket-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1LinkTicketResponse](../../doc/models/protos-openapi-v1-link-ticket-response.md).

## Example Usage

```csharp
string deploymentId = "123";
LinkTicketRequest body = new LinkTicketRequest
{
    DeploymentId = "123",
    IssueIds = new List<string>
    {
        "issue_ids0",
        "issue_ids9",
    },
    TicketUrl = "https://myorg.atlassian.net/browse/SEC-123",
};

try
{
    ApiResponse<ProtosOpenapiV1LinkTicketResponse> result = await ticketingServiceApi.LinkTicketAsync(
        deploymentId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Unlink Ticket

Remove the ticket association from one or more Semgrep findings by providing a list of finding IDs. This does not delete the ticket in your issue tracker — it only removes the association in Semgrep.

```csharp
UnlinkTicketAsync(
    string deploymentId,
    Models.UnlinkTicketRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`UnlinkTicketRequest`](../../doc/models/unlink-ticket-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1UnlinkTicketResponse](../../doc/models/protos-openapi-v1-unlink-ticket-response.md).

## Example Usage

```csharp
string deploymentId = "123";
UnlinkTicketRequest body = new UnlinkTicketRequest
{
    DeploymentId = "123",
    IssueIds = new List<string>
    {
        "issue_ids0",
        "issue_ids9",
    },
};

try
{
    ApiResponse<ProtosOpenapiV1UnlinkTicketResponse> result = await ticketingServiceApi.UnlinkTicketAsync(
        deploymentId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Create Ticket

Create Jira tickets for your findings. You can create tickets by passing in a list of issue_ids or by passing in filter query parameters to dynamically select findings. If passing in filters, Semgrep will skip already ticketed findings. This endpoint is synchronous, so it may take some time for your request to resolve. Unlike creating tickets in-app, if ticket creation fails we won't automatically retry. This endpoint accepts a limit parameter (defaulting to 20) to limit the number of tickets created per request. If you specify a list of issue_ids greater than this limit, or your selected filters match on a number of issues greater than this limit, issues that were not ticketed are included in the Failed part of the response object. You can send another request to create tickets for these skipped issues. By default, findings belonging to the same repository and the same rule will be grouped together into a single Jira ticket. You can override this using the group_issues query parameter. Up to 50 issues can be grouped into a single ticket. You can optionally override the Jira project you create tickets in by passing in a Jira project ID as jira_project_id (the numeric ID rather than the project key). You can fetch this ID using the Jira API.

```csharp
CreateTicketAsync(
    string deploymentSlug,
    Models.CreateTicketRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `body` | [`CreateTicketRequest`](../../doc/models/create-ticket-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ProtosOpenapiV1CreateTicketResponse](../../doc/models/protos-openapi-v1-create-ticket-response.md).

## Example Usage

```csharp
string deploymentSlug = "deploymentSlug6";
CreateTicketRequest body = new CreateTicketRequest
{
    DeploymentSlug = "deploymentSlug2",
    IssueType = IssueType1.Sca,
    AutotriageVerdict = AutotriageVerdict.TruePositive,
    Categories = new List<string>
    {
        "security",
        "performance",
    },
    ComponentTags = new List<string>
    {
        "user authentication",
        "user data",
    },
    Confidence = Confidence3.High,
    Dependencies = new List<string>
    {
        "lodash",
        "express",
    },
    GroupIssues = true,
    IncludeHistorical = true,
    IssueIds = new List<string>
    {
        "issue_ids6",
        "issue_ids7",
    },
    JiraProjectId = "12345",
    Limit = 20L,
    Policies = new List<string>
    {
        "rule-board-block",
        "rule-board-pr-comments",
        "rule-board-audit",
    },
    ProOnly = true,
    ProjectTags = new List<string>
    {
        "my_project_tag_1",
        "my_project_tag_2",
    },
    MRef = "refs/pull/1234/merge",
    Repos = new List<string>
    {
        "myorg/repo1",
        "myorg/repo2",
    },
    Rules = new List<string>
    {
        "typescript.react.security.audit.react-no-refs.react-no-refs",
        "ajinabraham.njsscan.hardcoded_secrets.node_username",
    },
    Ruleset = new List<string>
    {
        "owasp-top-ten",
        "default",
    },
    SecretTypes = new List<string>
    {
        "Github",
        "Heroku",
        "AWS",
    },
    Since = "1717334400",
    Status = Status1.Open,
};

try
{
    ApiResponse<ProtosOpenapiV1CreateTicketResponse> result = await ticketingServiceApi.CreateTicketAsync(
        deploymentSlug,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```

