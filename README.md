 <div align="right"><a href="#english">🇬🇧 EN</a> | <a href="#turkish">🇹🇷 TR</a></div>

# ECommerceDemo

<a id="english"></a>

## Overview

**ECommerceDemo** is a microservices-based e-commerce application built with ASP.NET Core and .NET. The project explores how e-commerce capabilities can be separated into independently organized services, with dedicated components for API routing, authentication, product catalog management, shopping baskets, orders, discounts, and supporting operations.

The solution brings together backend services and an MVC-based web interface to demonstrate service-oriented application design and communication between distributed components.

## Architecture

The repository is organized around the following components:

| Component | Responsibility |
|---|---|
| **API Gateway** | Routes incoming requests through Ocelot |
| **Identity Server** | Authentication and identity management using IdentityServer4 and ASP.NET Core Identity |
| **Catalog Service** | Product catalog and product data management |
| **Basket Service** | Shopping basket operations, with Redis integration |
| **Order Service** | Order-related application logic |
| **Discount Service** | Discount management |
| **Cargo Service** | Shipping and cargo-related operations |
| **Payment Service** | Dedicated payment service component |
| **Comment Service** | Product comment-related functionality |
| **Image Service** | Image-related operations |
| **Message Service** | Message management |
| **RabbitMQ Service** | Messaging integration using RabbitMQ |
| **SignalR Service** | Real-time communication using SignalR |
| **Web UI** | ASP.NET Core MVC-based web application |
| **Rapid API** | Additional API and integration component |

> The repository contains services with different levels of implementation. The presence of a service does not necessarily mean that every business workflow is fully integrated or production-ready.

## Technology Stack

- **Backend:** C#, ASP.NET Core, .NET 6
- **Architecture:** Microservices, API Gateway
- **API Gateway:** Ocelot
- **Authentication:** IdentityServer4, ASP.NET Core Identity, JWT Bearer Authentication
- **Databases and Data Access:** Microsoft SQL Server, MongoDB, PostgreSQL, Entity Framework Core, Dapper
- **Caching:** Redis
- **Messaging:** RabbitMQ
- **Real-Time Communication:** SignalR
- **Web Application:** ASP.NET Core MVC
- **Object Mapping:** AutoMapper
- **API Documentation:** Swagger / Swashbuckle

## Key Concepts

- Separating business capabilities into individual services
- Routing requests through a centralized API Gateway
- Implementing authentication and identity-related workflows
- Using different data stores according to service requirements
- Integrating cache and message-broker technologies
- Supporting real-time communication
- Organizing a multi-project .NET solution

## Repository Structure

```text
ECommerceDemo/
├── ApiGateway/
├── IdentityServer/
├── Services/
│   ├── Basket/
│   ├── Cargo/
│   ├── Catalog/
│   ├── Comment/
│   ├── Discount/
│   ├── Images/
│   ├── Message/
│   ├── Order/
│   ├── Payment/
│   ├── RabbitMQ/
│   └── SignalRRealTime/
├── Frontends/
│   ├── ECommerce.DtoLayer/
│   └── Ecommerce.WebUI/
├── RapidApi/
└── ECommerce.sln
```

## Getting Started

### Prerequisites

Install the following tools before running the solution:

- Visual Studio 2022 or a compatible .NET development environment
- .NET 6 SDK
- The database and infrastructure services required by the individual projects, such as SQL Server, MongoDB, Redis, or RabbitMQ

### Installation

Clone the repository:

```bash
git clone https://github.com/onuraydi/ECommerceDemo.git
cd ECommerceDemo
```

Open `ECommerce.sln` in Visual Studio and restore the NuGet dependencies.

### Configuration

Before running individual services:

1. Review each service's `appsettings.json` and development configuration.
2. Configure database connection strings and infrastructure endpoints for your local environment.
3. Set up the identity provider, gateway routes, and authentication settings required for service-to-service communication.
4. Configure any required external services before starting the corresponding projects.

**Security note:** Do not commit real credentials, connection strings, signing keys, or other secrets to source control. Use user secrets or environment variables for local development.

### Running the Application

The solution contains multiple independently configured projects. Start the required infrastructure services first, then launch the Identity Server, API Gateway, relevant backend services, and web application using their respective configurations.

The exact startup sequence and available workflows depend on the configuration of each service.

## Development Notes

This repository targets **.NET 6**, which has reached end of support. For new deployments, consider upgrading to a supported .NET release and reviewing the compatibility of the associated packages.

IdentityServer4 is also a legacy identity platform. Review its maintenance status and migration options before using this implementation in a production environment.

## Purpose

ECommerceDemo serves as a practical codebase for exploring microservices architecture, distributed application components, authentication, data access, caching, messaging, and real-time communication in the .NET ecosystem.

---

<a id="turkish"></a>

# Türkçe

## Genel Bakış

**ECommerceDemo**, ASP.NET Core ve .NET kullanılarak geliştirilmiş, mikroservis mimarisini temel alan bir e-ticaret uygulamasıdır. Proje; e-ticaret işlevlerinin ayrı servisler halinde organize edilmesini, servisler arası iletişimi ve farklı altyapı bileşenlerinin bir arada kullanılmasını ele alır.

Çözüm; API yönlendirme, kimlik doğrulama, ürün kataloğu, sepet, sipariş, indirim ve diğer destekleyici işlevler için ayrı bileşenler içerir. Backend servisleri, ASP.NET Core MVC tabanlı web arayüzüyle birlikte yapılandırılmıştır.

## Mimari

Depodaki temel bileşenler ve sorumlulukları:

| Bileşen | Sorumluluk |
|---|---|
| **API Gateway** | Ocelot üzerinden gelen isteklerin yönlendirilmesi |
| **Identity Server** | IdentityServer4 ve ASP.NET Core Identity ile kimlik yönetimi |
| **Catalog Service** | Ürün kataloğu ve ürün verilerinin yönetimi |
| **Basket Service** | Redis entegrasyonu içeren sepet işlemleri |
| **Order Service** | Sipariş süreçlerine ilişkin uygulama mantığı |
| **Discount Service** | İndirim yönetimi |
| **Cargo Service** | Kargo ve gönderim işlemleri |
| **Payment Service** | Ödeme işlemleri için ayrılmış servis bileşeni |
| **Comment Service** | Ürün yorumlarıyla ilgili işlevler |
| **Image Service** | Görsel işlemleri |
| **Message Service** | Mesaj yönetimi |
| **RabbitMQ Service** | RabbitMQ ile mesajlaşma entegrasyonu |
| **SignalR Service** | SignalR üzerinden gerçek zamanlı iletişim |
| **Web UI** | ASP.NET Core MVC tabanlı web uygulaması |
| **Rapid API** | Ek API ve entegrasyon bileşeni |

> Depoda yer alan servislerin uygulama kapsamları aynı seviyede olmayabilir. Bir servisin mevcut olması, ilgili iş akışının bütünüyle tamamlandığı veya üretim ortamına hazır olduğu anlamına gelmez.

## Teknoloji Yığını

- **Backend:** C#, ASP.NET Core, .NET 6
- **Mimari:** Mikroservis mimarisi, API Gateway
- **API Gateway:** Ocelot
- **Kimlik Doğrulama:** IdentityServer4, ASP.NET Core Identity, JWT Bearer Authentication
- **Veritabanları ve Veri Erişimi:** Microsoft SQL Server, MongoDB, PostgreSQL, Entity Framework Core, Dapper
- **Önbellekleme:** Redis
- **Mesajlaşma:** RabbitMQ
- **Gerçek Zamanlı İletişim:** SignalR
- **Web Uygulaması:** ASP.NET Core MVC
- **Nesne Eşleme:** AutoMapper
- **API Dokümantasyonu:** Swagger / Swashbuckle

## Öne Çıkan Teknik Konular

- İşlevlerin bağımsız servisler halinde ayrıştırılması
- İsteklerin merkezi API Gateway üzerinden yönlendirilmesi
- Kimlik doğrulama ve kimlik yönetimi süreçleri
- Servis gereksinimlerine göre farklı veri depolarının kullanılması
- Önbellekleme ve mesaj aracısı entegrasyonu
- Gerçek zamanlı iletişim altyapısı
- Çok projeli .NET çözümünün organizasyonu

## Proje Yapısı

```text
ECommerceDemo/
├── ApiGateway/
├── IdentityServer/
├── Services/
│   ├── Basket/
│   ├── Cargo/
│   ├── Catalog/
│   ├── Comment/
│   ├── Discount/
│   ├── Images/
│   ├── Message/
│   ├── Order/
│   ├── Payment/
│   ├── RabbitMQ/
│   └── SignalRRealTime/
├── Frontends/
│   ├── ECommerce.DtoLayer/
│   └── Ecommerce.WebUI/
├── RapidApi/
└── ECommerce.sln
```

## Kurulum

### Gereksinimler

- Visual Studio 2022 veya uyumlu bir .NET geliştirme ortamı
- .NET 6 SDK
- İlgili projelerin gerektirdiği SQL Server, MongoDB, Redis ve RabbitMQ gibi altyapı bileşenleri

### Depoyu Klonlama

```bash
git clone https://github.com/onuraydi/ECommerceDemo.git
cd ECommerceDemo
```

`ECommerce.sln` dosyasını Visual Studio ile açın ve NuGet bağımlılıklarını geri yükleyin.

### Yapılandırma

Servisleri çalıştırmadan önce:

1. Her servisin `appsettings.json` ve geliştirme ortamı yapılandırmalarını inceleyin.
2. Veritabanı bağlantılarını ve altyapı adreslerini yerel ortamınıza göre düzenleyin.
3. Kimlik sağlayıcısını, API Gateway yönlendirmelerini ve servisler arası kimlik doğrulama ayarlarını yapılandırın.
4. İlgili servisleri başlatmadan önce ihtiyaç duyulan harici altyapıları çalışır duruma getirin.

**Güvenlik notu:** Gerçek parolaları, bağlantı dizelerini, imzalama anahtarlarını ve diğer gizli bilgileri kaynak koduna eklemeyin. Yerel geliştirmede User Secrets veya ortam değişkenleri kullanın.

### Uygulamayı Çalıştırma

Çözüm birden fazla bağımsız yapılandırılmış proje içerir. Önce gerekli altyapı servislerini, ardından Identity Server, API Gateway, ihtiyaç duyulan backend servislerini ve web uygulamasını kendi çalıştırma ayarlarına göre başlatın.

Kesin başlatma sırası ve kullanılabilir iş akışları, servislerin yapılandırmasına bağlıdır.

## Geliştirme Notları

Proje **.NET 6** hedeflemektedir ve bu sürümün resmi destek süresi sona ermiştir. Yeni dağıtımlar için desteklenen bir .NET sürümüne geçiş ve bağımlılıkların uyumluluk kontrolü değerlendirilmelidir.

IdentityServer4 de eski bir kimlik platformudur. Üretim ortamında kullanılmadan önce bakım durumu ve geçiş seçenekleri incelenmelidir.

## Projenin Amacı

ECommerceDemo; .NET ekosisteminde mikroservis mimarisi, dağıtık uygulama bileşenleri, kimlik doğrulama, veri erişimi, önbellekleme, mesajlaşma ve gerçek zamanlı iletişim konularını incelemek için hazırlanmış bir kod tabanıdır.

