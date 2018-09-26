Commands:


"<Target Name="NSwag" BeforeTargets="Build">
   <Exec Command="$(NSwagExe) swagger2tsclient /input:cars-swagger.json /namespace:$(RootNamespace) /InjectHttpClient:true /UseBaseUrl:true /output:CarsClient.cs" />
</Target>"
