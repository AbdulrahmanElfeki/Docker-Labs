# first-stage base image  
FROM mcr.microsoft.com/dotnet/sdk:9.0 AS build
WORKDIR /source

# copy my sproj & restore dependencies
COPY *.csproj .
RUN dotnet restore

# copy & publish application files
COPY . .
RUN dotnet publish -c release -o /app

# final stage image 
FROM mcr.microsoft.com/dotnet/aspnet:9.0 
WORKDIR /app
COPY --from=build /app .

ENTRYPOINT [ "dotnet", "hrapp.dll" ]
