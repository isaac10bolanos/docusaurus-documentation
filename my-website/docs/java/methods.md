---
sidebar_position: 3
sidebar_label: 'Methods'
---

# Methods
## What is a method?

- A block of instructions.
- A block of code used to perform some operation.
- Which only runs when called by name.
- A method defines the behavior of a class.
- All methods must be defined inside the body of a class.

```jsx title="Example"
public class MyClass {

	public static int myFirstMethod(int x, int y) {
		return x+y;
    }
}
```

## Declaring a method

**A method declaration contains 6 parts:**
1. Accessor     (public)
2. modifiers(s)               (static)   optional
3. Return type             (int) not optional
4. Method Name        (myFirstMethod)  not optional
5. Parameters      (int x, int y)     optional must include ()
6. Body               (return x+y;)   

## Method signature 
Consists of the method name and parameters.

## Calling a method

The code inside your method will not run until it is called:
- By name
- Followed by parentheses
- With the correct number & type of values (arguments)

## Parameters
Are variables local to the method where they are defined.

## Arguments
Are values assigned to the parameter local variables when the method is called.

## Method Overloading

A class can have multiple methods with the same name.

Overloaded methods must have a different number or type of parameters.

```jsx title="Example"
public static void eat(String food, int qty) {

}
public static void eat(int qty, String food) {

}
```

## Method Overriding

Is taking the same method signature and parameters and replacing it with it's own implementation.

```jsx title="Cat class"
public class Cat {

	private String name;

	public Cat(String name) {
		this.name = name;
	}

	public void speak() {
		System.out.println(name + " likes to say Meow");
	}
}
```

```jsx title="Tiger class"
public class Tiger extends Cat {

	public Tiger(String name) {
		super(name);
	}

	@Override
	public void speak() {
		System.out.println(getName() + " does not say Meow, he ROARS!");
	}
}
```




