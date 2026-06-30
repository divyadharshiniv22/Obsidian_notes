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

### 1. GPS Coordinates

GPS coordinates represent a location on Earth using:

- **Latitude** → North/South position
- **Longitude** → East/West position

Example:

```
location = (13.0827, 80.2707)
```

Here:

- `13.0827` = Latitude of Chennai
- `80.2707` = Longitude of Chennai

Apps like **Google Maps**, Uber, and food delivery apps use GPS coordinates to locate places.

RGB colors are used to **display colors on digital screens** such as computers, phones, TVs, websites, and mobile apps.

### How it works

Screens create colors by mixing three light colors:

- **R** = Red
- **G** = Green
- **B** = Blue

Each value ranges from **0 to 255**.

Examples:

|Color|RGB Value|
|---|---|
|Red|(255, 0, 0)|
|Green|(0, 255, 0)|
|Blue|(0, 0, 255)|
|White|(255, 255, 255)|
|Black|(0, 0, 0)|
|Yellow|(255, 255, 0)|

### Real-world uses

#### Web Development

```
background-color: rgb(255, 0, 0);
```

This makes the background red.

#### Image Processing

A photo is made up of millions of pixels, and each pixel has an RGB value.

Example:

```
pixel = (255, 0, 0)
```

This pixel will appear red.

#### UI Design

Designers choose RGB values for buttons, icons, backgrounds, and text colors.

#### Games and Graphics

Game developers use RGB values to render colors for characters, objects, and environments.

### Why a tuple?

RGB always has **exactly 3 values** (Red, Green, Blue), so it is often stored as a tuple:

```
color = (255, 128, 64)
```

Here:

- Red = 255
- Green = 128
- Blue = 64

Together, these three values create a specific color on the screen.

The comma is what makes it a tuple.

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

![[Pasted image 20260622090436.png]]
 ```python
 if __name__ == "__main__": 
  
 - file name and terminal both are equal means it will excuted next line. call the main function.
   
 ```
2 line it will second line call the get_student() function. in 6 . line goes. 

input is the in build function value assigned in the name variable.

input is the build function value assigned in the name house variable.

return(name , house ) tuple unpacking.
assigned in the student variable. 

print formatted string 
output : dharshini from chennai.

 


