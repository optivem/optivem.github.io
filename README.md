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

Libraries for application core:

| Library | Interfaces | Abstract Base |
| ------------- | ------------- | ------------- |
| Entity | Optivem.Entity | Optivem.Entity.Base |
| Repository | Optivem.Repository | Optivem.Repository.Base |
| Service | Optivem.Service | Optivem.Service.Base |

Infrastructure libraries:

| Library | Interfaces | Abstract Base | Concrete Implementations | 
| ------------- | ------------- | ------------- | ------------- |
| Parser | Optivem.Parser | Optivem.Parser.Base | Optivem.Parser.Standard |
| Serialization | Optivem.Serialization | Optivem.Serialization.Base | Optivem.Serialization.Json <br> Optivem.Serialization.Xml <br> Optivem.Serialization.Csv |
| A | Optivem. | Optivem. | Optivem. |



### Optivem Java Libraries

Pending to be released. 

## Feedback

You can send questions, improvement suggestions and issue reports on [GitHub](https://github.com/optivem/optivem.github.io/issues/new). These will be used to further improve our open source software.

## License

Licensed under the [MIT license](http://opensource.org/licenses/mit-license.php). Copyright © 2018 [Optivem](https://www.optivem.com/) All Rights Reserved. 