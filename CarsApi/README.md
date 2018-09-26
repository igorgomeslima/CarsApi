Commands:

-----------------------------------------------------------------------------------------------------

- Instal HTTP REPL

dotnet tool install -g --version 2.2.0-* --add-source https://dotnet.myget.org/F/dotnet-core/api/v3/index.json dotnet-httprepl

- Package Manager Console

Add-Migration Initial -OutputDir Data/Migrations
Update-Database

- NSwag (MSBuild)

`<Target Name="NSwag" BeforeTargets="Build">
   <Exec Command="$(NSwagExe) swagger2tsclient /input:cars-swagger.json /namespace:$(RootNamespace) /InjectHttpClient:true /UseBaseUrl:true /output:CarsClient.cs" />
</Target>`

- Blazor Template

-To use Blazor Template
   - Minimum: .NET Core 2.1 SDK (2.1.302) and Visual Studio 2017 (15.7 or later)
   - Download and Install -> https://marketplace.visualstudio.com/items?itemName=aspnet.blazor

-----------------------------------------------------------------------------------------------------


><Target Name="NSwag" BeforeTargets="Build">
   <Exec Command="$(NSwagExe) swagger2tsclient /input:cars-swagger.json /namespace:$(RootNamespace) /InjectHttpClient:true /UseBaseUrl:true /output:CarsClient.cs" />
</Target>"

