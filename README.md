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

This enables your software development team to appropriately choose to depend on interfaces and within IoC container to configure implementations and execute unit testing. Furthermore, it also enables development teams to either choose to use the standard provided implementations or develop custom implementations.

## Optivem Libraries

### Optivem .NET Core 2 Libraries

Libraries for application core for business logic and data abstraction:

Interfaces | Abstract Bases | Concrete Implementations |
| ------------- | ------------- | -- |
| Entity | Entity.Base | N/A |
| Repository | Repository.Base | Repository.EntityFramework <br> Repository.Dapper <br> Repository.AdoNet <br> Repository.MongoDb <br> Repository.Cassandra |
| UnitOfWork | UnitOfWork.Base | UnitOfWork.EntityFramework <br> UnitOfWork.Dapper <br> UnitOfWork.AdoNet <br> UnitOfWork.MongoDb <br> UnitOfWork.Cassandra |
| Service | Service.Base | N/A |
| Controller | Controller.Base | N/A |

Infrastructure libraries for cross-cutting concerns:

Interface | Abstract Base | Concrete Implementations |
| ------------- | ------------- | ------------- |
| [Parser](https://opensource.optivem.com/csharp-parser/) | Parser.Base | Parser.Standard |
| Mapping | Mapping.Base | Mapping.Standard |
| Validation | Validation.Base | Validation.Standard |
| Serialization | Serialization.Base | Serialization.Json <br> Serialization.Xml <br> Serialization.Csv <br> Serialization.Excel |
| Logging | N/A  | Logging.Log4Net <br> Logging.NLog |
| Messaging | N/A | TBD |
| Identity | Identity.Base | Identity.AspNetIdentity |
| Authentication | N/A | Authentication.OAuth  |
| Authorization | N/A | Authorization.OAuth  |
| Workflow | N/A | TBD  |
| Queue | N/A | TBD  |
| Process | N/A | Process.Standard <br> Process.Remote  |
| Notification | N/A | Notification.SignalR  |

Infrastructure libraries for integration with external systems:

| Clock | N/A | Clock.Standard |
| FileSystem | N/A | FileSystem.Standard <br> FileSystem.Ftp |
| Email | N/A  | Email.Gmail <br> Email.Outlook <br> Email.SendGrid |
| Cloud | N/A  | Cloud.Azure <br> Cloud.Aws <br> Email.Google |
| RestClient | N/A  | RestClient.RestSharp |
| RestService | N/A  | RestService.AspNetCore |
| SoapClient | N/A  | TBD  |
| SoapService | N/A | TBD  |

<!-- TODO: VC: Check regarding PDF and also DSV, additionally UOW and also design patterns, e.g. factory and builder... azure.. amazon... configuration, testing, sql lite, NHibernate, DDD, CQRS, Domain... IoC -> AutoFac, Ninject, Unity, Kafka  -->


<!-- TODO: VC: Search infrastructure https://www.nuget.org/packages?page=8&q=infrastructure -->


### Optivem Java Libraries

Pending to be released. 

## Feedback

You can send questions, improvement suggestions and issue reports on [GitHub](https://github.com/optivem/optivem.github.io/issues/new). These will be used to further improve our open source software.

## License

Licensed under the [MIT license](http://opensource.org/licenses/mit-license.php). Copyright © 2018 [Optivem](https://www.optivem.com/) All Rights Reserved. 