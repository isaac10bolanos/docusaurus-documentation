---
sidebar_position: 3
sidebar_label: 'YAML'
---

# YAML

## What is YAML?

A Yaml file is used to represent data.  Below are configuration data represented in three different formats.

```jsx title="XML"
<Servers>
    <Server>
    <name>Server1</name>
    <owner>John</owner>
    <created>12232012</created>
    <status>active</status>
    </Server>
</Servers>
```

```jsx title="JSON"
{
    Servers: [
        {
        name: Server1,
        owner: John,
        created: 12232012,
        status: active,
        }
    ]
}
```

```jsx title="YAML"
Servers:
    -   name: Server1
        owner: John
        created: 12232012
        status: active
```

---

## Key Value Pair

```jsx title="Key Value Pair"
Fruit: Apple
Vegetable: Carrot
Liquid: Water
Meat: Chicken
```

**Rember to have a space between the colon to differentiate the Key and the Value.**

---

```jsx title="Array/Lists"
Fruits:
-   Orange
-   Apple
-   Banana

Vegetables:
-   Carrot
-   Cauliflower
-   Tomato
```

**The dash represents there is an element of an array.**

---

Dictionary:  Is a set of properties group together under an item.

Must have an equal amount of spacing between the properties.

```jsx title="Dictionary/Map"
Banana:
    Calories: 105
    Fat: 0.4 g
    Carbs: 27 g

Grapes:
    Calories: 62
    Fat: 0.3 g
    Carbs: 16 g
```

:::tip
**YAML rules are equal number of spaces.**
:::
