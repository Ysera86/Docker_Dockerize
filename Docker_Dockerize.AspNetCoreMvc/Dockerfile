FROM mcr.microsoft.com/dotnet/sdk:7.0
WORKDIR /app
COPY . .
RUN dotnet restore
RUN dotnet publish Docker_Dockerize.AspNetCoreMvc.csproj -c Release -o out
WORKDIR out
ENV ASPNETCORE_URLS="http://*:5043"
ENTRYPOINT ["dotnet","Docker_Dockerize.AspNetCoreMvc.dll"]