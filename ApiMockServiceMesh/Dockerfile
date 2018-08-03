FROM microsoft / aspnetcore-build
WORKDIR / app
COPY * .csproj.
RUN DotNet restaurar
COPY . .
Executar dotnet publicar --output / out / --configuration Release