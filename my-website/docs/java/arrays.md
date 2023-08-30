---
sidebar_position: 4
sidebar_label: 'Arrays'
---
# Arrays
## Definition
A container that holds a fixed number of values of a single type.

Each value has an index starting with 0

:::tip Index

Last index = length -1
:::


## Arrays in memory
Values are stored continuous in memory.

**zero -indexing**

Indexing start at 0 same as strings

## Array declaration
There are two ways to declare an array:

```
int[] myNumbers;

int myNumbers[];
```

## Array initialization

**There are two ways to initialize an array**
- Using the new operator
- Using an array literal

```
int[] myNumbers = new int[10];

int[] bigNums = {10000, 345, 890};
```

## Array new operator

The new operator allocates memory.

The contents of the array are initialized to default values.

```
int[] myNumbers = new int[6];
```

:::caution Keep in mind
Has to be the same type: int only int OR byte only byte
:::

## Array literals

An array literal is defined using {}

It sets the length to the given number of elements.

```
int[] myNumbers = {7, 3, 4, 5, 9};
```
**The length of array is 5.**

## Accessing array elements
To access an element in an array, use the index inside[]

```
int[] myNumbers = {7, 3, 4, 5, 9};

int a = myNumbers[0]; // 7

int b = myNumbers[2];  // 4

int c = myNumbers[4];  // 9
```

## Assigning values 
To assign a value to an element in an array, use the index inside []

```
myNumbers[0] = 10;

myNumbers[1] = 0;

myNumbers[4] = -8;
```

## Array exceptions

**ArrayIndexOutOfBoundsException**

Occurs when accessing an index out of bounds

## Array length

To access the length of the array, use .length

```
int[] nums = {7, 3, 4, 5, 9};

int size = nums.length;
```

:::note
There are no ( ) after **.length** because it is a **property** not a **method**.
:::

**Useful for accessing the last element**

```
int lastElement = nums[nums.length - 1];
```

## Reassignment

We can reassign an array.

```
int[] nums = {7, 3, 4, 5, 9};

nums = new int[10]; // valid 
```

**Array constants can only be used in initializers.**

```
int nums = {7, 3, 4, 5, 9};

nums = new int[10]; // valid          length = 10

nums = {7, 8, 9}; // invalid because already initialized

nums = new int[] {7, 8, 9}; // valid 
```

:::danger Watch out

```
String[] names = {“Bob”, “Sue”, “Joe”};

names[3] = “Tom”;
```
**This will throw an IndexOutOfBoundException**

**Because the last index is length - 1 = 2**
:::


















