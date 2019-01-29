## Introduction

Are you a leader in an enterprise software development organization, interested in producing quality software? Have you experienced the challenges in managing software projects - satisfying customers' needs to produce software faster, but yet at the same time, facing quality issues? Have you seen systems which rapidly deteriorated in quality, whereby the architecture is a "big ball of mud", and low code quality - and the decreased productivity of the whole team? Is there an increasing pile of bugs, and are changes taking longer and longer to implement, breaking existing functionality? Do you face challenges in incorporating new team members, increasing the technical level of your team, and incorporating code standards and quality control? 

Are you looking for a solution which will enable you to:
* Implement high quality enterprise software in your software teams
* Increase the productivity across your team, from junior to senior level
* Support extensible and maintainable architecture to reduce total development cost

If you've answered "yes", then you've come to the right place. Welcome to Optivem Open Source Software (OSS).
Our goal is to support you in quality Enterprise Application Software (EAS) development.

## Architecture

The underlying architecture for our projects is based on the "Clean Architecture" approaches:
* [Hexagonal Architecture, aka. Ports and Adapters (Alistair Cockburn, 2005)](https://dzone.com/articles/hexagonal-architecture-is-powerful) 
* [Onion Architecture (Jeffrey Palermo, 2008)](https://jeffreypalermo.com/2008/07/the-onion-architecture-part-1/)
* [Clean Architecture (Robert C. Martin, 2012)](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)

For an introductory overview, we recommend [DDD, Hexagonal, Onion, Clean, CQRS, … How I put it all together](https://herbertograca.com/2017/11/16/explicit-architecture-01-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/).

<!-- TODO: VC: Describe the architectures -->

The key concept is the separation of concerns: 
* Application Core contains application logic (Application Layer) and domain logic (Domain Layer)
* Presentation Layer contains GUI Views and Controllers, REST Controllers, SOAP Controllers, Console Commands
* Infrastructure Layer contains Databases, Email, Messaging, and any other external agencies

The dependencies are as follows:
* The Application Core is independent of everything else (i.e. the Application Core does not know about the Presentation Layer nor the Infrastructure Layer)
* The Presentation Layer sends commands to the Application Core
* The Infrastructure Layer contains implementation for communicating with the database (e.g. via ORM, sending emails, sending messages to message queues, etc.)

But, given the independence above, how do they communicate? The answer is: Inversion of Control (IoC) - Dependency Injection (DI). For example, the Application Core defines interfaces for communicating with a database (i.e. Repository interfaces), and inside the Infrastructure layer, the Repository interfaces are implemented (e.g. using ORM frameworks or any other mechanisms).

The core benefits is that due to the independence of the Application Core, it ensures separation of concerns and modulaity, swappability of databases, UIs and any frameworks, and also enables the system to be testable. These factors increase system quality and decreasing overall total development and maintenance cost.



## Optivem Platform

The Optivem Platform is designed to support the clean architecture, enabling:
* Separation of concerns
* Independence of frameworks, DB, UI
* High component re-use
* Extensibility & flexibility
* Maintainability & testibility
* Scalability and portability

The Optivem Platform is on GitHub and NuGet: 

* [Optivem Platform (.NET Core 2.2) GitHub](https://opensource.optivem.com/platform-dotnetcore)
* [Optivem Platform (.NET Core 2.2) NuGet](https://www.nuget.org/profiles/optivem)

To show the Optivem Platform usage, we developed a sample application using the well-known Northwind database from Microsoft, as an illustration relevant for enterprise software samples:

* [Optivem Northwind (.NET Core 2.2)](https://opensource.optivem.com/northwind-dotnetcore)
* [Optivem Northwind (Angular 7)](https://opensource.optivem.com/northwind-angular)

## System Requirements

The following are the applications and technologies installed, which are required to run the projects above.

For .NET Core 2.2 projects, we installed [Microsoft .NET Core SDK 2.2.101](https://dotnet.microsoft.com/download) and used [Visual Studio Community 2017 Version 15.9.4](https://visualstudio.microsoft.com/vs/community/) for the development. For databases, we used [SQL Server Express 14.0](https://www.microsoft.com/en-us/sql-server/sql-server-editions-express) and [SQL Server Management Studio (SSMS) v17.8.1](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-2017).

For Angular 7 projects, we installed [Node.js](https://nodejs.org/en/), [Angular 7 CLI](https://cli.angular.io/), and [Angular 7](https://angular.io/). For development, we used [Visual Studio Code](https://code.visualstudio.com/) and the [Debugger for Chrome (Visual Studio Code Extension)](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome) .

Additional tools used include: [Postman 6.6.1](https://www.getpostman.com/apps).

## Feedback

You can send questions, improvement suggestions and issue reports on [GitHub](https://github.com/optivem/optivem.github.io/issues/new). These will be used to further improve our open source software.

## License

Licensed under the [MIT license](http://opensource.org/licenses/mit-license.php).

## Copyright

Copyright © 2019 [Optivem](https://www.optivem.com/) All Rights Reserved. 