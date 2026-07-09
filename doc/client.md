
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| Environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.Production`** |
| Timeout | `TimeSpan` | Http client timeout.<br>*Default*: `TimeSpan.FromSeconds(30)` |
| HttpClientConfiguration | [`Action<HttpClientConfiguration.Builder>`](../doc/http-client-configuration-builder.md) | Action delegate that configures the HTTP client by using the HttpClientConfiguration.Builder for customizing API call settings.<br>*Default*: `new HttpClient()` |
| LogBuilder | [`LogBuilder`](../doc/log-builder.md) | Represents the logging configuration builder for API calls |
| SemgrepAdminJwtCredentials | [`SemgrepAdminJwtCredentials`](auth/oauth-2-bearer-token.md) | The Credentials Setter for OAuth 2 Bearer token |
| SemgrepJwtCredentials | [`SemgrepJwtCredentials`](auth/oauth-2-bearer-token-1.md) | The Credentials Setter for OAuth 2 Bearer token |
| SemgrepWebTokenCredentials | [`SemgrepWebTokenCredentials`](auth/oauth-2-bearer-token-2.md) | The Credentials Setter for OAuth 2 Bearer token |

The API client can be initialized as follows:

## Code-Based Initialization

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

## Configuration-Based Initialization

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

See the [Configuration-Based Initialization](../doc/configuration-based-initialization.md) section for details.

## Semgrep Web AppClient Class

The gateway for the SDK. This class acts as a factory for the Apis and also holds the configuration of the SDK.

### Controllers

| Name | Description |
|  --- | --- |
| DeploymentsServiceApi | Gets DeploymentsServiceApi. |
| FindingsServiceApi | Gets FindingsServiceApi. |
| MiscServiceApi | Gets MiscServiceApi. |
| PoliciesServiceApi | Gets PoliciesServiceApi. |
| ProjectsServiceApi | Gets ProjectsServiceApi. |
| ScansServiceApi | Gets ScansServiceApi. |
| SecretsServiceApi | Gets SecretsServiceApi. |
| SupplyChainServiceApi | Gets SupplyChainServiceApi. |
| TicketingServiceApi | Gets TicketingServiceApi. |
| TriageServiceApi | Gets TriageServiceApi. |

### Properties

| Name | Description | Type |
|  --- | --- | --- |
| HttpClientConfiguration | Gets the configuration of the Http Client associated with this client. | [`IHttpClientConfiguration`](../doc/http-client-configuration.md) |
| Timeout | Http client timeout. | `TimeSpan` |
| Environment | Current API environment. | `Environment` |
| SemgrepAdminJwtCredentials | Gets the credentials to use with SemgrepAdminJwt. | [`ISemgrepAdminJwtCredentials`](auth/oauth-2-bearer-token.md) |
| SemgrepJwtCredentials | Gets the credentials to use with SemgrepJwt. | [`ISemgrepJwtCredentials`](auth/oauth-2-bearer-token-1.md) |
| SemgrepWebTokenCredentials | Gets the credentials to use with SemgrepWebToken. | [`ISemgrepWebTokenCredentials`](auth/oauth-2-bearer-token-2.md) |

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `GetBaseUri(Server alias = Server.Semgrep)` | Gets the URL for a particular alias in the current environment and appends it with template parameters. | `string` |
| `ToBuilder()` | Creates an object of the Semgrep Web AppClient using the values provided for the builder. | `Builder` |

## Semgrep Web AppClient Builder Class

Class to build instances of Semgrep Web AppClient.

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `HttpClientConfiguration(Action<`[`HttpClientConfiguration.Builder`](../doc/http-client-configuration-builder.md)`> action)` | Gets the configuration of the Http Client associated with this client. | `Builder` |
| `Timeout(TimeSpan timeout)` | Http client timeout. | `Builder` |
| `Environment(Environment environment)` | Current API environment. | `Builder` |
| `SemgrepAdminJwtCredentials(Action<SemgrepAdminJwtModel.Builder> action)` | Sets credentials for SemgrepAdminJwt. | `Builder` |
| `SemgrepJwtCredentials(Action<SemgrepJwtModel.Builder> action)` | Sets credentials for SemgrepJwt. | `Builder` |
| `SemgrepWebTokenCredentials(Action<SemgrepWebTokenModel.Builder> action)` | Sets credentials for SemgrepWebToken. | `Builder` |

