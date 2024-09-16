# Use the official .NET SDK image to build the application
# This image includes the .NET CLI and all necessary build tools
FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build

# Set the working directory inside the container
WORKDIR /app

# Copy the .csproj file and restore any dependencies
# Copy the .csproj file
COPY KubernetesAutoClusterAPI/KubernetesAutoClusterAPI.csproj ./KubernetesAutoClusterAPI/

# Restore the project dependencies
RUN dotnet restore KubernetesAutoClusterAPI/KubernetesAutoClusterAPI.csproj

# Copy the entire project to the container
COPY . .

# Build the application
RUN dotnet build kubernetesautoclusterapi/kubernetesautoClusterapi.csproj -c Release -o /app/build

# Publish the application
RUN dotnet publish kubernetesautoclusterapi/kubernetesautoClusterapi.csproj -c Release -o /app/publish

# Use the official .NET runtime image to run the application
# This image contains only the .NET runtime, making it lighter
FROM mcr.microsoft.com/dotnet/aspnet:7.0 AS runtime

# Set the working directory inside the container
WORKDIR /app

# Copy the published output from the build stage
COPY --from=build /app/publish .

# Set the entry point for the application
ENTRYPOINT ["dotnet", "kubernetesautoclusterapi.dll"]
