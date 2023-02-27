Inner components and how they interact with each other.

## Layers

Force well formed and focused code and increases modularity.
In theory you can switch out the UI layer or DAL.

Expose interfaces - UI or Service interface
Excuting logic - Business Logic
Saving / Retrieving data - Data access layer

Code only flows to the layer below. Keep the layers strict.

These layers should be losely coupled. Acheive this with dependecy injection and don't depend on concrete implementations.

Exception handling between layers.
eg Database exceptions should encapsulate their error and not pass implementation details to the calling layer and exposing the database technology.
It should log the exception and throw a helpful error to the caller layer.

## Interfaces

Defines your contracts and can allow different implementations of the contract.
Helps testability and allows dependency injection
Loosely coupled components.

## Dependency Injection

Great and should be used to create losely coupled code and components.
Dependencies can be swapped out.
Lifetimes can be controlled with the dependecy injection container.
Testability is acheived by mocking dependencies

## SOLID

Use common sense and be pragmatic. 
Sometimes duplication is ok

### Single responsibility

Each class should have a single responsbility and well defined function
Principle can be applied to services and components

### Open / Closed

Software entities should be extended without having to update and modify the code.
Inheritance is a technique that can be used.
Plugin mechanisms
Makes the code flexible and less prone to bugs as you don't have to modify the original code

### Liskov Substitution 

Polymorphism and sub typing should allow any of the substitutions should not change the behavior.
Avoid hidden behavior and unexpecting side effects.

### Interface Segregation

Make finely grained interfaces and think responsibility here too.
Split up large interfaces otherwise clients may be forced to create implementations that they do not need to have.

### Dependency Inversion

Common sense principle and leads you down the DI path which is a good thing for coupling, testability etc

## Naming Conventions

Important to define and stick to the convention. Different conventions will be popular dependent on the language you use.

Important thing here is to be consistent and name things well.

Class names should always be Nouns
- DataRetriever
- Customer
Method names should always be Verbs
- RetrieveData
- DeleteCustomer

## Exception Handling

Have a consistent method for reporting exceptions

- Only catch exceptions if you have something to do with it such as rollback a transaction or retrying
- Always catch specific exceptions so that you can report it and handle it correctly.
- Use a Try..Catch on the smallest code fragements possible.
- Never surround large chunks of code with Try..Catch

## Logging

Know what is going on with the system and make it easy to diagnose problems.

Use for two purposes

- Tracking errors
	- Know where to look for problems
- Gather data
	- What method gets used most
	- Performance
	- Usage of the system
	- Important Events
