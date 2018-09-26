# Sample project with "What's New in ASP.NET Core 2.2"

ASP.NET Core 2.2 features:

- Template updates: Bootstrap 4, Angular 6
- Web API improvements
- HTTP/2
- IIS in-process hosting
- Health checks
- Endpoint routing
- SignalR Java Client

-------------------------------------------

- Easier to create (API Scaffolding)
- Easier to test & debug (HTTP REPL, Problem Details)
- Easier to document (API convetions & analyzer)
- Easier to consume (Code genration (Preview 3))
- Easier to secure (Web API security (Preview 3))
- Easier to monitor (Health checks integration)
- Improved performance (HTTP/2, endpoint routing, IIS in-proc hosting).

S104 - What's New in ASP.NET Core? https://www.youtube.com/watch?v=DDBmvOPfqzA

-----------------------------------------------------------------------------------------------------

Instal HTTP REPL

dotnet tool install -g --version 2.2.0-* --add-source https://dotnet.myget.org/F/dotnet-core/api/v3/index.json dotnet-httprepl

Package Manager Console

Add-Migration Initial -OutputDir Data/Migrations
Update-Database

NSwag (MSBuild)

<Target Name="NSwag" BeforeTargets="Build">
   <Exec Command="$(NSwagExe) swagger2tsclient /input:cars-swagger.json /namespace:$(RootNamespace) /InjectHttpClient:true /UseBaseUrl:true /output:CarsClient.cs" />
</Target>

Blazor Template

-To use Blazor Template
   - Minimum: .NET Core 2.1 SDK (2.1.302) and Visual Studio 2017 (15.7 or later)
   - Download and Install -> https://marketplace.visualstudio.com/items?itemName=aspnet.blazor

-----------------------------------------------------------------------------------------------------
