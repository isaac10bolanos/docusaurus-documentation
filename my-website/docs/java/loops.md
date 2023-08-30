---
sidebar_position: 5
sidebar_label: 'Loops'
---
# Loops
## What is a loop?

A loop is a **control-flow statement** that repeats a block of code until a condition is reached.

## While loop

Repeats a block of code while a condition is true.

```jsx title="Example"
int count = 3;     // setup

while (count > 0) {    // condition must be an expression that evaluates to a boolean
System.out.println(count);		// body
count = count -1;		// update
}

System.out.println(“Boom!”);
```

### Body
Must be surrounded by {}.

Otherwise, the loop ends at the first.

### Infinite loops

If the condition is always true, the loop never ends.

```
while (true) {
	// do something
}
```

:::important Keep in mind
- If the condition is initially false, the loop **never runs**.
- If the condition is always true, the loop **never ends**.
:::

## Do-while loop

Runs a block of code then repeats while a condition.

Do {something} while (condition);

Always runs at least once.

```jsx title="Example"
String[] birds = {"duck", "duck", "goose",
				  "duck", "duck", "duck"};
int i = 0;
do {
	System.out.println(birds[i]);
	i++;
} while(i < birds.length && !birds[i - 1].equals("goose"));
```

## For loop
Repeats a block of code **for** a set number of iterations.

Anything you can do with a **while** loop can be done with a for loop.

```jsx title="For loop notation"
for (int i = 0; i < 3; i++) {
	System.out.println(i);
}
```

**Same lines of code do the same exact thing**
```jsx title="For loop vs While loop"
for (int i = 0; i < 3; i++) {								int i = 0;
	System.out.println(i);									while (i < 3) {
}																System.out.println(i);
																i++;
															}
```

:::note
All 3 parts of the for-loop are optional but the ; ; are required.
:::

## Enhanced for loop
Repeats a block of code for each element in a collection.

Also known as **for-each** loop.

:::important
**Pro: useful when you do not need the index.**

**Con: you cannot update the elements.**
:::

```jsx title="Enhanced for notation"
int[] nums = { 1, 2, 3 };

for (int i : nums) {
	System.out.println(i);
}
```


