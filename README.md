# Scylum

[![NuGet Publishing](https://github.com/hypeproxy/orchestrator/actions/workflows/publish.yml/badge.svg)](https://github.com/hypeproxy/orchestrator/actions/workflows/publish.yml)
![Net8](https://img.shields.io/badge/.NET-8.0%20LTS-blue)
![MIT](https://img.shields.io/badge/MIT-License-yellow)

## Introduction

Scylum is a library designed to streamline the creation and management of services and controllers in .NET applications. It provides a set of classes and methods that standardize common operations within APIs, with flexible configuration options for routing and service responses.

With an intuitive and extensible API, here’s an overview of Scylum’s core features:

- **Unified Service Management**: Simplifies service creation and dependency injection, allowing services to interact with each other seamlessly.
- **Base Controller Wrapping**: Offers a standardized base controller to manage claims and user data access, reducing boilerplate code.
- **Routing Conventions**: Supports customizable routing conventions, including options like kebab-case for cleaner and more consistent URLs.
- **Standardized Result Handling**: Provides a unified response format with BaseResult to ensure consistent response handling across services.

## Getting Started

To get started with Scylum, follow these steps:

1. Installation: Add Scylum to your project via NuGet:

```bash
dotnet add package Scylum
```

2. Service Setup: In your `Program.cs`, register Scylum services and configure routing options:

```bash
var builder = WebApplication.CreateBuilder(args);

builder.Services.AddScylum(options =>
{
    options.RouteStyle = RoutingStyle.KebabCase; // Customize your routing style here
});

var app = builder.Build();
app.UseHttpsRedirection();
app.UseAuthorization();
app.MapControllers();
app.Run();
```
