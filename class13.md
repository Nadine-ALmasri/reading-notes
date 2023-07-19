

# Dependency Injection
Dependency Injection in ASP.NET Core is a design pattern that promotes loose coupling between components. It allows classes to receive required services as dependencies from the framework instead of creating them directly. This practice simplifies testing, improves maintainability, and enhances the flexibility and scalability of the application. By using the built-in dependency injection container, developers can easily register and resolve services across the application.


# Repository pattern


Repository pattern helps abstract data access and separate domain logic from data interactions. By using the Repository pattern, developers can easily switch between different data sources while maintaining the integrity of the application's business logic, leading to improved testability and flexibility in data storage technologies.



# Test-Driven Development (TDD)


Test-Driven Development (TDD) help making code SOLID. It emphasizes writing tests before writing the actual code to ensure code quality and adherence to the SOLID principles. The SOLID principles help create more maintainable, flexible, and scalable code by promoting good design practices such as Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion. By following TDD and SOLID principles, developers can build robust, high-quality software with improved maintainability and reduced bugs.

## The SOLID Principles
### S — Single Responsibility

A class should have a single responsibility ,If a Class has many responsibilities, it increases the possibility of bugs because making changes to one of its responsibilities, could affect the other ones without you knowing.
### O — Open-Closed
Classes should be open for extension, but closed for modification ,Changing the current behaviour of a Class will affect all the systems using that Class.

If you want the Class to perform more functions, the ideal approach is to add to the functions that already exist NOT change them.
### Liskov Substitution

If S is a subtype of T, then objects of type T in a program may be replaced with objects of type S without altering any of the desirable properties of that program.
### I — Interface Segregation

Clients should not be forced to depend on methods that they do not use.
### D — Dependency Inversion

- High-level modules should not depend on low-level modules. Both should depend on the abstraction.

- Abstractions should not depend on details. Details should depend on abstractions.
















[Home](./README.md)  