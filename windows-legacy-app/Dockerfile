FROM microsoft/dotnet-framework:4.6.2

WORKDIR /app

COPY publish /app

EXPOSE 9000

ENTRYPOINT ["dotnet", "windows-legacy-app.dll"]
