## Introduction

Welcome to Optivem Open Source Software (OSS), designed to support Enterprise Application Software (EAS) development. This contains a set of libraries designed to solve common technical needs in enterprise software development. 

### Purpose

The purpose of Optivem OSS is to help IT organizations to:
* Empower high performance development teams
* Support extensible and maintainable architecture
* Implement high quality enterprise software

### Architecture

The overall architectural approach is oriented towards Clean Architecture, especially the Onion architecture and Hexagonal Architecture approaches, where IoC is a fundamental element, separating the application core from infrastructure code. 

The Optivem libraries are designed to support these architectures, with separation of concerns and maximal re-use, enabling:
* Extensibility & flexibility
* Maintainability & testibility
* Scalability and portability. 

Each library is split into:
* Interfaces
* Abstract base classes
* Concrete implementations

This enables your software development team to appropriately choose to depend on interfaces and within IoC container to configure implementations and execute unit testing. Furthermore, it also enables development teams to either choose to use the default provided implementations or develop custom implementations.

## Project Websites


* [Platform (.NET Core 2.2)](https://opensource.optivem.com/platform-dotnetcore)
* [Northwind (.NET Core 2.2)](https://opensource.optivem.com/northwind-dotnetcore)

## Optivem Libraries

### Optivem .NET Core 2 Libraries

Libraries for application core for business logic and data abstraction:

| Interfaces | Implementations |
| ------------- | ------------- |
| Entity | Entity.Default |
| Repository | Repository.EntityFramework <br> Repository.Dapper <br> Repository.AdoNet <br> Repository.MongoDb <br> Repository.Cassandra |
| UnitOfWork | UnitOfWork.EntityFramework <br> UnitOfWork.Dapper <br> UnitOfWork.AdoNet <br> UnitOfWork.MongoDb <br> UnitOfWork.Cassandra |
| Service | Service.Default |
| Controller | Controller.Default |

Infrastructure libraries for cross-cutting concerns:

| Interface | Implementations |
| ------------- | ------------- |
| Parsing | Parsing.Default |
| Mapping | Mapping.Default |
| Validation | Validation.Default |
| Serialization | Serialization.Json <br> Serialization.Xml <br> Serialization.Csv <br> Serialization.Excel |
| Logging | Logging.Log4Net <br> Logging.NLog |
| Messaging | TBD |
| Identity | Identity.AspNetIdentity |
| Authentication | Authentication.OAuth  |
| Authorization | Authorization.OAuth  |
| Workflow | TBD  |
| Queue | TBD  |
| Process | Process.Default <br> Process.Remote  |
| Notification | Notification.SignalR <br> Notification.Email |
| Configuration | Configuration.Default  |

Infrastructure libraries for integration with external systems:

| Interface | Implementations |
| ------------- | ------------- |
| Clock | Clock.Default |
| FileSystem | FileSystem.Default <br> FileSystem.Ftp |
| Email | Email.Gmail <br> Email.Outlook <br> Email.SendGrid |
| Cloud | Cloud.Azure <br> Cloud.Aws <br> Email.Google |
| RestClient | RestClient.RestSharp |
| RestService | RestService.AspNetCore |
| SoapClient | TBD |
| SoapService | TBD |

<!-- TODO: VC: Check regarding PDF and also DSV, additionally UOW and also design patterns, e.g. factory and builder... azure.. amazon... configuration, testing, sql lite, NHibernate, DDD, CQRS, Domain... IoC -> AutoFac, Ninject, Unity, Kafka  -->


<!-- TODO: VC: Search infrastructure https://www.nuget.org/packages?page=8&q=infrastructure -->


### Optivem Java Libraries

Pending to be released. 

## Instructions

# C# Instructions

* Visual Studio Community 2017 Version 15.9.4 - [Download Visual Studio Community Version](https://visualstudio.microsoft.com/vs/community/)
* SQL Server Express 14.0 - [Download SQL Server Express](https://www.microsoft.com/en-us/sql-server/sql-server-editions-express)
* SQL Server Management Studio v17.8.1 - [Download SQL Server Management Studio (SSMS)](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-2017)
* Microsoft .NET Core SDK 2.2.101 - [Download .NET Core SDK](https://dotnet.microsoft.com/download)

# Java Instructions

Pending

# Angular Instructions

* Visual Studio Code - [Download Visual Studio Code](https://code.visualstudio.com/)
* Visual Studio Code - Extension - [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome) 
* Node.js - [Download Node.js](https://nodejs.org/en/)
* Angular 7 CLI - [Download Angular CLI](https://cli.angular.io/)
* Angular 7 - [Download Angular](https://angular.io/) 

For installation instructions, see the following tutorial [Angular 7 Tutorial: Building CRUD Web Application](https://www.djamware.com/post/5bca67d780aca7466989441f/angular-7-tutorial-building-crud-web-application)

# Other Tools

* Postman 6.6.1 - [Download Postman](https://www.getpostman.com/apps)

## Feedback

You can send questions, improvement suggestions and issue reports on [GitHub](https://github.com/optivem/optivem.github.io/issues/new). These will be used to further improve our open source software.

## License

Licensed under the [MIT license](http://opensource.org/licenses/mit-license.php). Copyright © 2018 [Optivem](https://www.optivem.com/) All Rights Reserved. 
