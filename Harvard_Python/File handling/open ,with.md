# `open()` in Python

 `open()` is used to open a file for reading, writing, or appending.


# Syntax

```
open(filename, mode)
```

---

# Example

```python
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

```python
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

```python
file = open("note.txt","w")

file.write("the python is much easier than others.\n")

file.write("AI can replace the job ! \n")

file.close()
```

Creates or overwrites file content.

---

# Append to a File

```python
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

```python
data =

 {

  "name" = "DHARSHINI",

  "age" = 23,

  "weight" = 67

  

 }

print(json.dumps(data,indent = 4,sort_key =True))


-> json dictionary
```

```python
import csv  
  
name = input("What's your name? ")  
home = input("Where's your home? ")  
  
with open("students.csv", "a") as file:  
writer = csv.writer(file)  
writer.writerow()
```

### CSV Library

The CSV library only provides:

```python

csv.reader()
csv.DictReader()
csv.writer()

```

There is no:

```python

csv.append()

```