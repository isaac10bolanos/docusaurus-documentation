---
sidebar_position: 3
sidebar_label: 'Select Queries'
---

# Select Queries

## Syntax

- Main main MaIn MaiN - in java these are 4 different things

- In SQL they are the same thing, SQL is not case sensitive for keywords

- Statements in SQL end in ;

- Whitespace does not matter, but semi-colons do

**Anytime you want to grab data you use a SELECT query**

```jsx title="Examples:"
SELECT * FROM artist;

seLect * from ArTiSt; # this is the exact same query as above
```

## Defining

**Select queries are always:**

SELECT <**What?**> FROM <**Where?**>

The **Where** needs to be accessible in the current table.

Same with the **What**.

## Wildcard

In SQL **(*)** is a wildcard that means "ALL" or "EVERYTHING"

```
SELECT * FROM track;
```

## Selecting multiple columns

I can specify the specific columns I want in my **SELECT** queries.

If I am selecting multiple columns they need to be comma separated.

```
SELECT Name, Composer, UnitPrice FROM track;
```

:::important Note
**The order I query for columns is the order they are returned in.**
:::

## Filter

I can filter the data that is returned by my select queries.

To filter I must use a **WHERE** clause.

SELECT <**What?**> FROM <**Where?**> WHERE <**something is true**>

```
SELECT * FROM track WHERE TrackId > 3000;

SELECT * FROM track WHERE TrackId = 200;
```

**Where clauses use the same logical operators we use in Java**

- Greater than >

- Less than <

- = equal to (not a ==)

- Greater than or equal to <=

- Less than or equal to <= 

