---
sidebar_position: 7
sidebar_label: 'Exceptions'
---

# Exceptions

## Unchecked Exceptions

Some unforeseen thing happened, something Java does not know how to recover from.

These happen at runtime / compile time you can recover from exceptions, but you need to tell Java how exceptions you can recover from errors you cannot.

### ArithmeticException

```jsx title="Example"
int var = 0;

int result = 5 / var;
```

### ArrayIndexOutOfBoundException

```jsx title="Example"
int[] nums = {2, 3, 5, 6};

nums[5] = 7;
```

## Try-catch statement

You can try-catch statement to handle exceptions.

Wrap risky code inside the try { } and then your error handling code inside the catch() { }

:::note
You NEED a **Catch** for every **Try.**
:::

```jsx title="ArithmeticException example:"
try {
	int var = 0;
	int result = 5 / var;  
	System.out.println("Math works"); // this will not run if an exception is thrown
} catch(ArithmeticException ex) {
	// if the code above didn't work because of an arithmetic exception run this
	// need to tell the catch what to look for
	System.out.println("Someone mathed wrong here!");
}
```

## Exception class

This is a catch all basically. it needs to be last, if it is not last it creates unreachable code.

The order of the catches matters.

```jsx title="Exception class"
try {
	int val = 0;
	int[] vals = { 1, 2 };
	int result = 3 / vals[3]; 
} catch(Exception ex) {
	// I can't get very specific without knowing what the exception is
	System.out.println("Will always catch an exception");
}
```

## Finally block

You can only have one finally block, and it always run.

Any code that needs to happen regardless of if you run successfully or not.

```jsx title="Finally block"
try {
	int var = 0;
	int result = 5 / var;  
	System.out.println("Math works"); // this will not run if an exception is thrown
} catch(ArithmeticException ex) {
	// if the code above didn't work because of an arithmetic exception run this
	// need to tell the catch what to look for
	System.out.println("Someone mathed wrong here!");
} finally {
    System.out.println("This runs regardless of what happens.");
}
```

## Checked Exceptions

Throws keyword is used to signal other developers that I throw an exception.

This creates a checked exception.

Anything that isn't an error or a runtime exception is checked.

Can list out multiple exceptions as being thrown by your method.




 

