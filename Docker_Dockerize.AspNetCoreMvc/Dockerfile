FROM mcr.microsoft.com/dotnet/sdk:7.0 as base
WORKDIR /app
COPY /bin/Release/net7.0/publish .
ENTRYPOINT ["dotnet","Docker_Dockerize.AspNetCoreMvc.dll"]