<pre><Target Name="NSwag" AfterTargets="Build">
    <Exec Command="$(NSwagExe) webapi2swagger /assembly:$(OutDir)/MyWebAssembly.dll /controller:MyNamespace.MyController /output:swagger.json" />
    <Exec Command="$(NSwagExe) swagger2tsclient /input:swagger.json /output:Scripts/MyController.ts" />
</Target></pre>
