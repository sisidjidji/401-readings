# READ 08

- An interface contains definitions for a group of related functionalities that a non-abstract class or a struct must implement. An interface may define static methods, which must have an implementation. Beginning with C# 8.0, an interface may define a default implementation for members. An interface may not declare instance data such as fields, auto-implemented properties, or property-like events.

- An interface has the following properties:

* An interface is typically like an abstract base class with only abstract members. Any class or struct that implements the interface must implement all its members. Optionally an interface may define default implementations for some or all of its members.
* An interface can't be instantiated directly. Its members are implemented by any class or struct that implements the interface.
* A class or struct can implement multiple interfaces. A class can inherit a base class and also implement one or more interfaces.

- An interface has the following properties:

- An interface is typically like an abstract base class with only abstract members. Any class or struct that implements the interface must implement all its members. Optionally, an interface may define default implementations for some or all of its members.
An interface can't be instantiated directly. Its members are implemented by any class or struct that implements the interface.
A class or struct can implement multiple interfaces. A class can inherit a base class and also implement one or more interfaces.