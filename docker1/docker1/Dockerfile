FROM microsoft/dotnet:2.1-sdk As builder
WORKDIR /source
COPY *.csproj .
RUN dotnet restore
COPY . .
RUN dotnet publish --output /app/ --configuration Release
WORKDIR /app
ENTRYPOINT ["dotnet", "Api.dll"]