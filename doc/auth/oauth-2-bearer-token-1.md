
# OAuth 2 Bearer token



Documentation for accessing and setting credentials for SemgrepJWT.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| AccessToken | `string` | The OAuth 2.0 Access Token to use for API requests. | `AccessToken` | `AccessToken` |



**Note:** Auth credentials can be set using `SemgrepJwtCredentials` in the client builder and accessed through `SemgrepJwtCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```csharp
using SemgrepWebApp.Standard;
using SemgrepWebApp.Standard.Authentication;

namespace ConsoleApp;

SemgrepWebAppClient client = new SemgrepWebAppClient.Builder()
    .SemgrepJwtCredentials(
        new SemgrepJwtModel.Builder(
            "AccessToken"
        )
        .Build())
    .Build();
```


