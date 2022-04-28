## HTTPClient.Study

Sample of a project using HTTPClient to connnect any external API using best practices.

## Usings

- .NET 6
- Blazor
- System.Net.Http.JSON


## Basic Steps for beginners

1. Configure new service using `AddHttpClient()`;
2. Add NuGet Package for **System.Net.Http.JSON**. This will be useful ahead;
3. Collect the raw API JSON return and create the model for it (in VS you can Paste Special as JSON -> Class);
3.1. Clean the class if needed;
4. Set a new REQUEST using `HttpRequestMessage, according to address, content and verb;
5. Set the CLIENT using Factory (`IHttpClientFactory` to declare and `CreateClient()` to instance);
6. Call the api using `SendAsync` (remember to use ASYNC / AWAIT) and wait for response;
7. Check for sucess on response using `IsSucessStatusCode`;
8. On sucess, use AWAIT (again!) to read the content using `ReadFromJsonAsync` (remember to set using for the System.Net.Http.JSON)
9. On failure, work according to the house rules. (U can check ReasonPhrase);
10. To consume the info your received, check for error first, and for the response on second, after all this, u can work with the data received.

### Power Refactory

- Use `GetFromJsonAsync` or `PostFromJsonAsync` to produce less lines. But you must use `try...catch` on this one.
- Add URI base address on Program.cs

## References

- [iamtimcorey.com](http://www.iamtimcorey.com)
- HTTPClient on MS documentation
- [Code samples migrated in .NET 6](https://docs.microsoft.com/en-us/aspnet/core/migration/50-to-60-samples?view=aspnetcore-6.0)