FROM mcr.microsoft.com/dotnet/sdk:7.0 as build 
WORKDIR /app
COPY *.csproj .
RUN dotnet restore
COPY . .
RUN dotnet publish Docker_Dockerize.AspNetCoreMvc.csproj -c Release -o out

FROM mcr.microsoft.com/dotnet/aspnet:7.0
WORKDIR /app
COPY --from=build /app/out . 
ENV ASPNETCORE_URLS="http://*:5044"
ENTRYPOINT ["dotnet","Docker_Dockerize.AspNetCoreMvc.dll"]