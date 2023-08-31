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

## Where clauses

I can filter the data that is returned by my select queries.

To filter I must use a **WHERE** clause.

SELECT <**What?**> FROM <**Where?**> WHERE <**something is true**>

```
SELECT * FROM track WHERE TrackId > 3000;

SELECT * FROM track WHERE TrackId = 200;
```

### Logical operators

- Greater than >
- Less than <
- = equal to (not a ==)
- Greater than or equal to <=
- Less than or equal to <= 

```
SELECT * FROM track WHERE TrackId >= 3000;

SELECT * FROM track WHERE TrackId <= 1000;
```

### Additional logical opeators

- ! -> in SQL it is **NOT**
- || -> in SQL it is **OR**
- && -> in SQL it is **AND**

```
SELECT * FROM track WHERE AlbumId > 200 AND AlbumId < 300;

SELECT * FROM track WHERE NOT UnitPrice = 0.99;

SELECT * FROM track WHERE Composer = 'Green Day' OR Composer = 'Pearl Jam';
```

:::tip Note
**Select statements retrieve, but never change data.**
:::

## Order by clause

You can use an order by clause to re-order the data that is returned.

**ORDER BY** can use two more keywords and those are:

- **ASC** - Ascending order
- **DESC** - Descending order

```
SELECT * FROM invoice WHERE Total > 4.00 ORDER BY total DESC;

SELECT * FROM invoice WHERE BillingCountry = 'USA' ORDER BY BillingState;
```

## Wildcards for Like clause

**Can use wild cards to select in the case of being unsure of spelling or to pattern match.**

Two main wildcards you use to match Strings:

- % mean any number of characters, the placement does matter
- _ means any one character, the placement does matter

To search/pattern match on Strings you use the **LIKE** keyword

---

```
SELECT * FROM track WHERE Composer LIKE '%Steven Tyler%';
```
**The above says select every columns from Track where the Composer has Stephen Tyler in it.**

---

---
```
SELECT * FROM track WHERE Composer LIKE '%A%' ORDER BY Composer;
```
**Grab every column from Track where Composer starts with the letter A**

---

---

```
SELECT * FROM track WHERE Composer LIKE '_C%' ORDER BY Composer DESC;
```
**Grab every column from Track where the second character of Composer is C and only 2 characters long**

---