A **tuple** is an **ordered, immutable collection of items**.

- **Ordered**: items keep their position.
- **Immutable**: once created, you generally cannot add, remove, or change elements.
- Can contain elements of different types.

Example in Python:

```python

t = (1, "apple", 3.14)
print(t[0])  # 1
```

Key differences from a list in Python:

| Feature                             | Tuple | List  |
| ----------------------------------- | ----- | ----- |
| Ordered                             | Yes   | Yes   |
| Mutable                             | No    | Yes   |
| Syntax                              | `( )` | `[ ]` |
| Hashable (if contents are hashable) | Yes   | No    |

### Quick Summary

```python

()  - Empty tuple

(5,)- One element 

tuple(1,2,3)- Multiple element tuple

x,y=(10,20)-Tuple unpacking
```

EXAMPLE :

### 1. Student Record

A student's details can be stored as a tuple because they usually don't change frequently.

```Python

student = (101, "Divya", "ECE", 8.03)
print(student)
```

Output:

```python

(101, 'Divya', 'ECE', 8.03)
```

### Why use a tuple?

Suppose you store a date:

```python

date = (21, 6, 2026)
```

A date should not accidentally change, so a tuple is better than a list because tuples are immutable.

**Interview answer:**  

"A tuple is used to store related data that should not be modified, such as database records, coordinates, RGB colors, and dates."

.

### Without the comma

```
a = (5)
```

Python sees this as just the number `5` inside parentheses.

```
print(type(a))
```

Output:

```
<class 'int'>
```

---

### With the comma

```
a = (5,)
```

Python sees this as a tuple containing one element.

```
print(type(a))
```

Output:

```
<class 'tuple'>
```

---

### Why?

Parentheses alone don't create a tuple. The **comma** does.

Examples:

```
a = 1, 2, 3print(type(a))
```

Output:

```
<class 'tuple'>
```

Even without parentheses, it's still a tuple because of the commas.

---

### Easy way to remember

- `(5)` → Integer `5`
- `(5,)` → Tuple with one item: `5`

 ![[Pasted image 20260711005714.png]]

 ```python
 if __name__ == "__main__": 
  
 - file name and terminal both are equal means it will excuted next line. call the main function.
   
 ``
2 line it will second line call the get_student() function. in 6 . line goes. 

input is the in build function value assigned in the name variable.

input is the build function value assigned in the name house variable.

return(name , house ) tuple unpacking.
assigned in the student variable. 

print formatted string 
output : dharshini from chennai.

 


