# 4. Dockerfile Deep Dive

This is one of the most important parts of the project.

We used a **multi-stage build**. That is a best practice in modern containerization.

```dockerfile
FROM mcr.microsoft.com/dotnet/sdk:10.0 AS build
WORKDIR /app

COPY *.csproj .
RUN dotnet restore

COPY . .
RUN dotnet publish -c Release -o out

FROM mcr.microsoft.com/dotnet/runtime:10.0
WORKDIR /app

COPY --from=build /app/out .

ENTRYPOINT ["dotnet", "ConsoleApp1.dll"]
```

### Why multi-stage?

**Stage 1 – Build**
- Uses the full .NET SDK image
- Restores packages
- Compiles and publishes the application

**Stage 2 – Runtime**
- Uses only the slim runtime image
- Copies just the published output from the build stage
- Results in a much smaller and more secure final image

### Benefits we gain

- Smaller image size
- Fewer attack surfaces (no compilers or SDKs in production)
- Faster pulls and starts
- Clear separation between build environment and runtime environment
- Fully reproducible builds

This is exactly how production-grade cloud-native services are packaged.
