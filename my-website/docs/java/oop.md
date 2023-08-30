---
sidebar_position: 6
sidebar_label: 'Object Oriented Programming'
---

# Object Oriented Programming

## Class
- Blueprints for real life entities
- “Custom data types”
- Attributes of entity
- Capabilities of entity

## Object
- Specific instance of class
- Distinct properties from other objects 
- Created using a class

```jsx title="Defining an Object"
public class Person {

    String name;
    short heightInches;
    String favoriteFood;
    String favoriteSport;
}
```

## Constructors

- Code that is run right when the object is created.
- Triggered by using the **new** keyword.
- Typically handles the initialization and validation logic.
- May be overloaded like any other method.
- If no constructor is defined, Java creates a **“default constructor”** for the class.
- Initializes all properties with their default values.

```jsx title="Constructor setup"
public class Person {

    String name;
    short heightInches;
    String favoriteFood;
    String favoriteSport;

    public Person(String name, short heighInches, String favoriteFood, String favoriteSport) {
        this.name = name;
        this.heightInches = heightInches;
        this.favoriteFood = favoriteFood;
        this.favoriteSport = favoriteSport;
    }
}
```

```jsx title="Constructor initializer"
public static void main(String[] args) {
    Person mark = new Person("Mark", (short) 60, "Doughnuts", "Soccer");
}
```

## Static
- Static methods/properties belong to the class itself.
- No object is required for referencing it.
    - Not static methods may only be calling using an instance of the class.
- Shared between all instances of an object.
- Only one copy of it exists in memory.

## This
- A keyword that refers to the object that called the function or the object that is being created if its the constructor.
- May only be used inside a non-static function.
- Optional in most circumstance, but is advised for code clarity.

# 4 Pillars of OOP

## Inheritance
- Useful for subsets of another class.
- Share properties and methods from the class with the subclass.
- Creates and IS-A relationship with parent class.
- Promotes code reuse.
- Method overriding available when necessary.
- In java, every class automatically extends from the OBJECT class.

## Encapsulation
- Data hiding.
- Add read/write restrictions to object properties.
- Control access to specific methods of an object via access modifiers.
- Limit accessing data only through designated **getter** methods.
- Limit mutating data only through designated **setter** methods.
- Standard procedure is to make all properties **private** or **protected** and write a **public** getter and setter method to read/write it.
    - getter/setter naming convention should ALWAYS be the property name with the first letter capitalized and prefixed with get/set respectively
- Limiting access helps prevent accidental updates to data.

```jsx title="Encapsulation example"
public class Bird {

    private String color;

    public String getColor() {
        return this.color;
    }

    public void setColor(String color) {
        this.color = color;
    }
}
```

| Modifier | Class | Package | Subclass | Global |
| -------- | :---- | :------ | :------- | :----- |
| **Public** | Yes | Yes | Yes | Yes |
| **Protected** | Yes | Yes | Yes | No |
| **Default** | Yes | Yes | No | No |
| **Private** | Yes | No | No | No |

## Abstraction

- Hiding implementation details
- Simple user interface
- Facade
- Achieved via interfaces

## Polymorphism

- “Many forms”
- Method overloading
- Allows for different entities to be grouped together
- Since every class extends from Object, every class is polymorphic

## Interface vs Abstract classes

### Interface

- Outline a “contract” of capabilities that a class must implement
- May only contain abstract methods and static properties/methods
    - Abstract methods contain no implementation details
- Cannot be instantiated
- A class can implement multiple interfaces
- Classes that implement an interface MUST give an implementation for each abstract method or itself be an abstract class
- Typically named as an action or is prefixed with an “I”
    - Callable
    - IEntity

```jsx title="Defining an Interface"
public interface Driveable {
    public void drive();
}
```
```jsx title="Implemented class"
public class Car implements Driveable {
    
    @Override
    public void drive() {
        System.out.println("Vroom vroom!");
    }
}
```

### Abstract classes

- Similar to an interface, but may contain non-abstract methods
- Abstract methods MUST be labeled as **abstract**
- Cannot be instantiated
- May have constructor, but cannot be directly called with new
- Classes that extend an abstract class MUST give an implementation for each abstract method or itself be an abstract class

```jsx title="Defining an Abstract class"
public abstract class Animal {

    String name;

    public abstract void speak();

    @Override
    public String toString() {
        return this.name;
    }
}
```





