#READ4 


# WHAT IS A PROPERTY??

A property is a member that provides a flexible mechanism to read, write, or compute the value of a private field. Properties can be used as if they are public data members, but they are actually special methods called accessors. This enables data to be accessed easily and still helps promote the safety and flexibility of methods.

- Properties enable a class to expose a public way of getting and setting values, while hiding implementation or verification code.

- A get property accessor is used to return the property value, and a set property accessor is used to assign a new value. These accessors can have different access levels. For more information, see Restricting Accessor Accessibility.

- The value keyword is used to define the value being assigned by the set accessor.

- Properties can be read-write (they have both a get and a set accessor), read-only (they have a get accessor but no set accessor), or write-only (they have a set accessor, but no get accessor). Write-only properties are rare and are most commonly used to restrict access to sensitive data.

- Simple properties that require no custom accessor code can be implemented either as expression body definitions or as auto-implemented properties.



# OBJECT AND CLASSES

- Classes are declared by using the class keyword followed by a unique identifier

- A class defines a type of object, but it is not an object itself. An object is a concrete entity based on a class, and is sometimes referred to as an instance of a class.

- When a class declares a base class, it inherits all the members of the base class except the constructors

- When the object is created, enough memory is allocated on the managed heap for that specific object, and the variable holds only a reference to the location of said object

- If you don't provide a constructor for your class, C# creates one by default that instantiates the object and sets member variables to the default values as listed in the Default values of C# types article

- A constructor is a method whose name is the same as the name of its type
-A class or struct can also have a static constructor, which initializes static members of the type. Static constructors are parameterless