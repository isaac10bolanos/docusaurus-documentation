---
sidebar_position: 4
sidebar_label: 'Arrays'
---

# Definition
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

int[] myNumbers = new int[6];

Has to be the same type: int only int ; byte only byte




