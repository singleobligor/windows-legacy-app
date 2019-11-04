FROM microsoft/dotnet-framework:4.6.2

WORKDIR /app

COPY publish /app

EXPOSE 8000

ENTRYPOINT ["dotnet", "windows-legacy-app.dll"]
