
# Get Started

## Getting the Configuration

To authenticate against an OAuth2 provider, some specific data is needed. This data can usually be found on
the provider's developer portal for an application.
1. `Response Code`, is usually `code`.
2. `Client ID`, a unique ID for your app.
3. `Client Secret`, not always needed. As mobile devices aren't secure, the `Client Secret` is not secret. It is called a [Public OAuth Client](https://oauth.net/2/client-types/). Note that providers that have specific configuration for mobile don't request it.
4. `Scope`, for the scopes you want to obtain from the provider.
5. `Redirect URL`, in the case of mobile auth, it is most commonly a URL scheme redirecting to the application.
6. `Additional Parameters`, if the provider requires additional data that doesn't follow the OAuth standard.

Once you found this data, you can start implementing the authentication with the plugin.

> For iOS, custom URL Schemes used for `Redirect URL` can be set in the project's configuration. They will automatically be inserted in the `info.plist` file of your app by the plugin.

## C++
This step is not required if you don't plan to use the plugin with C++.

Open `<YourProject>.Build.cs` and add the following line in your module's constructor:

```csharp
PrivateDependencyModuleNames.Add("OAuth2");
```
