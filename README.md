# 🔗 URL Shortener with Analytics (gRPC Backend)

This project is a cloud-native **URL Shortener service** built using:
- 🧠 **.NET 8** with **gRPC**
- ☁️ Hosted on **Azure Container Apps**
- 🔐 Integrated with **Azure Key Vault** and **Azure Table Storage**
- 🐳 Containerized using **Docker**

It allows users to shorten URLs and track click analytics securely and efficiently.

---

## ✨ Features

- 🔗 Shorten long URLs with a unique code
- 📊 Track analytics (click count, timestamp, IP address, etc.)
- 🛡️ Secured secrets via **Azure Key Vault**
- 📁 Storage backed by **Azure Table Storage**
- 🌐 Supports both **gRPC** and **gRPC-Web** (via `EnableGrpcWeb`)
- 🚀 Container-ready for cloud deployments

---

## ⚙️ Technologies Used

| Layer | Tech |
|-------|------|
| Backend | `ASP.NET Core 8`, `gRPC`, `Grpc.AspNetCore.Web` |
| Security | `Azure.Identity`, `Azure.Security.KeyVault.Secrets` |
| Storage | `Azure.Data.Tables` |
| Deployment | `Docker`, `Azure Container Apps` |
| Tools | `BloomRPC`, `grpcurl`, `Postman` (with gRPC plugin) |

---

## 📐 Architecture

```plaintext
Client (gRPC / gRPC-Web)
      ↓
ASP.NET Core gRPC Service (.proto)
      ↓
URLShortenerServiceImpl
      ↓
Azure Table Storage (for mapping & analytics)
      ↓
Azure Key Vault (for secrets)
