
# Getting Started with Semgrep Web App

## Introduction

Welcome to Semgrep's portal for the Semgrep AppSec Platform web API.

### Introduction

Semgrep is a fast, open-source, static analysis tool for finding bugs and enforcing code standards at editor,
commit, and CI time. [Get started.](https://semgrep.dev/docs/getting-started/)

This API is documented in the **OpenAPI format**.

### Authentication

The API supports authentication with an API token with the "Web API" permission, without limited
scopes of access.

You can provision an API token [from the Settings page](https://semgrep.dev/orgs/-/settings/tokens).

### Terms of Use

Please note, the materials made available herein are subject to the
[Semgrep Terms of Use](https://semgrep.dev/resources/website-terms/), and your
access or use of any of the same is your acknowledgment and acceptance of the
such terms.

<br>


___


## Install the Package

If you are building with .NET CLI tools then you can also use the following command:

```bash
dotnet add package ApimaticsemgrepSDK --version 0.0.1
```

You can also view the package at:
https://www.nuget.org/packages/ApimaticsemgrepSDK/0.0.1

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| Environment | [`Environment`](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/README.md#environments) | The API environment. <br> **Default: `Environment.Production`** |
| Timeout | `TimeSpan` | Http client timeout.<br>*Default*: `TimeSpan.FromSeconds(30)` |
| HttpClientConfiguration | [`Action<HttpClientConfiguration.Builder>`](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/http-client-configuration-builder.md) | Action delegate that configures the HTTP client by using the HttpClientConfiguration.Builder for customizing API call settings.<br>*Default*: `new HttpClient()` |
| LogBuilder | [`LogBuilder`](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/log-builder.md) | Represents the logging configuration builder for API calls |
| SemgrepAdminJwtCredentials | [`SemgrepAdminJwtCredentials`](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token.md) | The Credentials Setter for OAuth 2 Bearer token |
| SemgrepJwtCredentials | [`SemgrepJwtCredentials`](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token-1.md) | The Credentials Setter for OAuth 2 Bearer token |
| SemgrepWebTokenCredentials | [`SemgrepWebTokenCredentials`](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token-2.md) | The Credentials Setter for OAuth 2 Bearer token |

The API client can be initialized as follows:

### Code-Based Initialization

```csharp
using Microsoft.Extensions.Logging;
using SemgrepWebApp.Standard;
using SemgrepWebApp.Standard.Authentication;

namespace ConsoleApp;

SemgrepWebAppClient client = new SemgrepWebAppClient.Builder()
    .SemgrepAdminJwtCredentials(
        new SemgrepAdminJwtModel.Builder(
            "AccessToken"
        )
        .Build())
    .SemgrepJwtCredentials(
        new SemgrepJwtModel.Builder(
            "AccessToken"
        )
        .Build())
    .SemgrepWebTokenCredentials(
        new SemgrepWebTokenModel.Builder(
            "AccessToken"
        )
        .Build())
    .HttpClientConfig(httpClientConfig =>
        httpClientConfig.Timeout(TimeSpan.FromSeconds(100)))
    .Environment(SemgrepWebApp.Standard.Environment.Production)
    .LoggingConfig(config => config
        .LogLevel(LogLevel.Information)
        .RequestConfig(reqConfig => reqConfig.Body(true))
        .ResponseConfig(respConfig => respConfig.Headers(true))
    )
    .Build();
```

### Configuration-Based Initialization

```csharp
using SemgrepWebApp.Standard;
using Microsoft.Extensions.Configuration;

namespace ConsoleApp;

// Build the IConfiguration using .NET conventions (JSON, environment, etc.)
var configuration = new ConfigurationBuilder()
    .AddJsonFile("config.json")
    .AddEnvironmentVariables() // [optional] read environment variables
    .Build();

// Instantiate your SDK and configure it from IConfiguration
var client = SemgrepWebAppClient
    .FromConfiguration(configuration.GetSection("SemgrepWebApp"));
```

See the [Configuration-Based Initialization](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/configuration-based-initialization.md) section for details.

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| Production | **Default** |

## Authorization

This API uses the following authentication schemes.

* [`SemgrepAdminJWT (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token.md)
* [`SemgrepJWT (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token-1.md)
* [`SemgrepWebToken (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token-2.md)

## List of APIs

* [Deployments Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/deployments-service.md)
* [Findings Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/findings-service.md)
* [Misc Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/misc-service.md)
* [Policies Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/policies-service.md)
* [Projects Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/projects-service.md)
* [Scans Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/scans-service.md)
* [Secrets Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/secrets-service.md)
* [Supply Chain Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/supply-chain-service.md)
* [Ticketing Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/ticketing-service.md)
* [Triage Service](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/controllers/triage-service.md)

## SDK Infrastructure

### Configuration

* [Configuration-Based Initialization](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/configuration-based-initialization.md)
* [HttpClientConfiguration](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/http-client-configuration.md)
* [HttpClientConfigurationBuilder](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/http-client-configuration-builder.md)
* [LogBuilder](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/log-builder.md)
* [LogRequestBuilder](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/log-request-builder.md)
* [LogResponseBuilder](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/log-response-builder.md)
* [ProxyConfigurationBuilder](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/proxy-configuration-builder.md)

### HTTP

* [HttpCallback](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/http-callback.md)
* [HttpContext](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/http-context.md)
* [HttpRequest](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/http-request.md)
* [HttpResponse](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/http-response.md)
* [HttpStringResponse](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/http-string-response.md)

### Utilities

* [ApiException](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/api-exception.md)
* [ApiResponse](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/api-response.md)
* [ApiHelper](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/api-helper.md)
* [CustomDateTimeConverter](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/custom-date-time-converter.md)
* [UnixDateTimeConverter](https://www.github.com/sdks-io/apimatic-semgrep-dotnet-sdk/tree/0.0.1/doc/unix-date-time-converter.md)

