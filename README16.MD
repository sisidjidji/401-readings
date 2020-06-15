
## Repository:

- Repositories are classes or components that encapsulate the logic required to access data sources. They centralize common data access functionality, providing better maintainability and decoupling the infrastructure or technology used to access databases from the domain model layer. 

- For each aggregate or aggregate root, you should create one repository class. In a microservice based on Domain-Driven Design (DDD) patterns, the only channel you should use to update the database should be the repositories. 

- repository allows you to populate data in memory that comes from the database in the form of the domain entities. Once the entities are in memory, they can be changed and then persisted back to the database through transactions.

- The difference between the Repository pattern and the legacy Data Access class (DAL class) pattern A data access object directly performs data access and persistence operations against storage. A repository marks the data with the operations you want to perform in the memory of a unit of work object (as in EF when using the DbContext class), but these updates aren't performed immediately to the database.




# SOLID Principles

1. Single Responsibility Principle:

The Single Responsibility Principal (SRP) is the idea that every method or class in your application should have exactly one reason to change. You can logically extend that to say that every class or method in your application should have exactly one (a single) job or responsibility. 

2. The Open/Close Principle:
IT's a Solid principle which states that the software entities (classes or methods) should be open for extension but closed for modification.

3. The Liskov Substitution Principle:
 It extends the Open/Closed principle and enables you to replace objects of a parent class with objects of a subclass without breaking the application. This requires all subclasses to behave in the same way as the parent class.

 4. The Interface Segregation Principle:
 states that no client should be forced to depend on methods it does not use.
 ISP splits interfaces that are very large into smaller and more specific ones so that clients will only have to know about the methods that are of interest to them. Such shrunken interfaces are also called role interfaces.

 5. The Dependency Inversion Principle:
 
 he dependency inversion principle is a specific form of decoupling software modules. When following this principle, the conventional dependency relationships established from high-level, policy-setting modules to low-level, dependency modules are reversed, thus rendering high-level modules independent of the low-level module implementation details.


