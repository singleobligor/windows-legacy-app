# STAGE01 - Build application and its dependencies
FROM microsoft/dotnet-framework:4.6.2

WORKDIR /app
COPY windows-legacy-app/*.csproj ./
COPY . ./
# RUN dotnet restore 

# STAGE02 - Publish the application
FROM build-env AS publish
RUN dotnet publish -c Release -o /app

# STAGE03 - Create the final image
FROM microsoft/dotnet-framework:4.6.2
WORKDIR /app
LABEL Author="Jitendra Singh"
COPY --from=publish /app .

EXPOSE 8000

ENTRYPOINT ["dotnet", "windows-legacy-app.dll"]
