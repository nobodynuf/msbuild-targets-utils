# msbuild-targets-utils

Donde subo distintos targets (que se utilizan en archivos de proyecto csproj) para situaciones concretas.

## ¿Que es un csproj?

Es una estructura de proyecto que se utiliza en proyectos .NET (C#/VB.NET) y, ahora, también en .NETCore. Son archivos XML con convenciones especificas.

## ¿Qué significa SDK y no-SDK?

Se refiere a que se utiliza la nueva estructuración de proyectos, que viene de la mano con proyectos .NETCore. Estos proyectos tienen más flexibilidad que los proyectos no-SDK (en ejemplo pero no limitado a: modificar el archivo de proyecto al estar usandolo en Visual Studio). Los proyectos SDK son compatibles con Visual Studio 2017 o superiores.

## ¿Cómo dijiste que ocupaba esto?

Agrega en cualquier parte de tu archivo csproj la etiqueta `<Import Project="$(SolutionDir)archivo.targets" />`. Esto considerando que dejaste los archivos `.targets` en la carpeta raíz de la solución. En caso que lo hayas dejado en una carpeta dentro de la solución (como por ejemplo, `build`) entonces la etiqueta cambia a ` <Import Project="$(SolutionDir)build\archivo.targets" />`.

## ¿No hay algo más que necesite saber?

Puedes leer sobre importar proyectos [aquí.](https://docs.microsoft.com/en-us/visualstudio/msbuild/import-element-msbuild?view=vs-2019)

[Acá](https://docs.microsoft.com/en-us/dotnet/core/tools/csproj) puedes leer de las diferencias entre proyectos que usan SDK y los que no.
