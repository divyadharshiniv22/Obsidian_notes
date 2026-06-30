# Nested Loops in Python

## Definition

A nested loop means:

> a loop inside another loop.

---

# Basic Structure

```
for outer_variable in outer_loop:    for inner_variable in inner_loop:        statement
```

---

# Simple Example

```
for i in range(3):    for j in range(2):        print(i, j)
```

---

# Output

```
0 00 11 01 12 02 1
```

---

# Step-by-Step Explanation

## Outer Loop

```
for i in range(3)
```

Runs:

```
0 → 1 → 2
```

---

## Inner Loop

```
for j in range(2)
```

Runs:

```
0 → 1
```

for every outer loop iteration.

---

# How Nested Loop Works

## First Outer Iteration

```
i = 0
```

Inner loop runs fully:

```
j = 0j = 1
```

Output:

```
0 00 1
```

---

## Second Outer Iteration

```
i = 1
```

Inner loop runs again:

```
1 01 1
```

---

## Third Outer Iteration

```
i = 2
```

Inner loop runs again:

```
2 02 1
```

---

# Visualization

```
i = 0    j = 0    j = 1i = 1    j = 0    j = 1i = 2    j = 0    j = 1
```

---

# Real-Life Example

## Students and Subjects

```python
students = ["Divya", "Subha"]
subjects = ["Python", "SQL"]
for student in students:    
for subject in subjects:        print(student, subject)
```

---

# Output

```python 
Divya Python
Divya SQL
Subha Python
Subha SQL
```

---

# Explanation

For every student:

- all subjects are printed.

---

# Nested Loop with List of Dictionaries

```
employees = [    {        "name": "Divya",        "skills": ["Python", "SQL"]    },    {        "name": "Subha",        "skills": ["Java", "AWS"]    }]
```

---

# Example

```
for employee in employees:    print(employee["name"])    for skill in employee["skills"]:        print(skill)
```

---

# Output

```
DivyaPythonSQLSubhaJavaAWS
```

---

# Step-by-Step

## First Employee

```
employee["name"]
```

Output:

```
Divya
```

---

## Inner Loop

```
employee["skills"]
```

contains:

```
["Python", "SQL"]
```

Inner loop prints:

```
PythonSQL
```

---

# Important Concept

```
Outer loop runs onceInner loop completes fully every time
```

---

# Common Uses of Nested Loops

- matrix operations
- pattern printing
- tables
- JSON/API data
- list of dictionaries
- data analysis

---

# Easy Memory Trick

```
For every outer item,do all inner items.
```

---

# Simple Meaning

```
Loop inside another loop
```

is called:

```
Nested Loop
```

def main():
    print_square(3)


def print_square(size):

    for i in range(size):

        for j in range(size):
            print("#", end="")

        print()


main()