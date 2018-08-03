FROM microsoft/dotnet:2.1-sdk
ADD . /src
EXPOSE 8080

WORKDIR /src

RUN dotnet restore -s http://nuget.cnova.com/nuget -s https://api.nuget.org/v3/index.json

WORKDIR /src/ApiMockServiceMesh

RUN dotnet publish -c Release -o /app

WORKDIR /app

ENTRYPOINT dotnet ApiMockServiceMesh.dll
