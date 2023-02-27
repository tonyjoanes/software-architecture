Here are a few useful ones to remember and keep in mind. Of course there are many more that could be used.

Take a common sense approach to using the patterns and only use where they are really applicable. Its also useful to know these and the names so that developers can have a common language and understanding when communicating with each other.

Patterns are really important to developers so they are important for Architects to understand them and when and where they should be used.

## Factory Pattern
Creation of objects without specifying the class types.
Usage of interfaces and reduce the `new` keyword in code.
**New is Glue**
This is very similar with using a DI container and being able to change implementations of interfaces.

The key change might be where we want to make a decision on which implementation to return from a factory.

Avoid strong coupling with this pattern.

## Repository Pattern
One of the most widely used patterns.
Is used as a data abstraction technique.

```csharp
public class WeatherService
{
	public WeatherService(IWeatherDataRepository weatherDataRepository)
	{
		this.weatherDataRepository = weatherDataRepository;
	}
	...
}
```

We do not have to depend on the underlying database technology. This weather data can come from MongoDB, MSSQL or even an in memory database.

## Facade Pattern
Create a layer of abstraction over complex actions.
Can be used to simplify multiple actions into a simple action to the clients.

## Command Pattern
Useful for capturing commands and being able to undo certain commands as they're all encapsulated within an object.