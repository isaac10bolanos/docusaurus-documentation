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
Wrap risky code inside the try { } and then your error
Handling code inside the catch() { } you NEED a catch for every try



 

