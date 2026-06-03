# `open()` in Python

 `open()` is used to open a file for reading, writing, or appending.


# Syntax

```
open(filename, mode)
```

---

# Example

```
file = open("data.txt", "r")
```

Meaning:

```
Open data.txt in read mode
```

---

# Common Modes

|Mode|Meaning|
|---|---|
|`"r"`|Read file|
|`"w"`|Write file|
|`"a"`|Append to file|
|`"x"`|Create new file|
|`"rb"`|Read binary file|
|`"wb"`|Write binary file|

---

# Read a File

Suppose `data.txt` contains:

```
Hello Python
```

Code:

```
file = open("data.txt", "r")
print(file.read())
file.close()
```

Output:

```
Hello Python
```

---

# Write a File

```
file = open("data.txt", "w")
file.write("Hello World")
file.close()
```

Creates or overwrites file content.

---

# Append to a File

```
file = open("data.txt", "a")
file.write("\nPython")
file.close()
```

Adds content at the end.

```python
name = input("What's your name? ")  
  
file = open("names.txt", "a")  
file.write(name)  
file.close()
```

Think of it like:

```python

Open notebook
Write something
Close notebook
```