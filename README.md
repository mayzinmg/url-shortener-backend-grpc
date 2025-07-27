# URL Shortener gRPC Service

![.NET](https://img.shields.io/badge/.NET-8.0-blue)
![gRPC](https://img.shields.io/badge/gRPC-supported-green)
![Azure](https://img.shields.io/badge/Azure-Table_Storage-blue)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A gRPC-based microservice that shortens long URLs and stores them using Azure Table Storage.

## Features

- ✅ gRPC API (Shorten, Expand, Analytics)
- ☁️ Azure Table Storage with `Azure.Data.Tables`
- 🐳 Dockerized for container deployment
- 🔒 Secure Key Vault access with `DefaultAzureCredential`

## Folder Structure

```
Protos/           → gRPC definitions (.proto)
Services/         → gRPC service implementation
Factories/        → Singleton factories (e.g., TableClient)
Models/           → Data models
```

## Getting Started

### 1. Build the Project

```bash
dotnet build
```

### 2. Run the Service

```bash
dotnet run
```

### 3. gRPC Testing Tools

- [BloomRPC](https://github.com/bloomrpc/bloomrpc)
- [grpcurl](https://github.com/fullstorydev/grpcurl)

---

## Docker

### Build Docker Image

```bash
docker build -t urlshortener-grpc .
```

### Run

```bash
docker run -p 5243:8080 urlshortener-grpc
```

## Environment Configuration

Set `KeyVaultName` in `appsettings.json`:

```json
{
  "KeyVaultName": "your-keyvault-name"
}
```

---

## License

MIT
