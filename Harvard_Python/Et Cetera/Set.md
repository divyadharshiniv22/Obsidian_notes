# List vs Tuple vs Set

| Feature          | List  | Tuple | Set   |
| ---------------- | ----- | ----- | ----- |
| Syntax           | `[]`  | `()`  | `{}`  |
| Ordered          | ✅ Yes | ✅ Yes | ❌ No  |
| Duplicate Values | ✅ Yes | ✅ Yes | ❌ No  |
| Mutable          | ✅ Yes | ❌ No  | ✅ Yes |
| Indexing         | ✅ Yes | ✅ Yes | ❌ No  |



A **set** is a collection that stores **unique values**.

It automatically removes duplicate values.

## Example

```python

numbers = {1, 2, 3, 4}

print(numbers)

```

Output:

```python

{1, 2, 3, 4}
```

---

## Duplicate Values

```python

numbers = {1, 2, 2, 3, 4, 4}

print(numbers)
```

Output:

```python

{1, 2, 3, 4}
```

**Why?**

A set **does not allow duplicates**.

# List vs Tuple vs Set

|List|Tuple|Set|
|---|---|---|
|`[]`|`()`|`{}`|
|Ordered|Ordered|Unordered|
|Duplicates Allowed|Duplicates Allowed|No Duplicates|
|Mutable|Immutable|Mutable|
|Indexing|Yes|Yes|

---

# Interview Definition

> **A set is an unordered, mutable collection of unique elements. It automatically removes duplicate values.**

## Easy Memory

```
List  → Ordered + Duplicates ✅

Tuple → Ordered + Fixed (Immutable)

Set   → Unique Values Only ❌ Duplicate
```
```python

fruits = {"mango","banana","grapes","apple"}

if "orange" in fruits:

print("yes mango is there")

else:

print("no the mango is not there")
```
