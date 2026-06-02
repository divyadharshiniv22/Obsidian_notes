Iteration with Lists in Python  
  
## What is Iteration?  [[for]]
  
Iteration means repeating a process one by one.



# Common Mistake

```python
student = ["dharshini", "dhemma", "puyyma"]

for study in student:
    print(student)
```

## Output

```python
['dharshini', 'dhemma', 'puyyma']
['dharshini', 'dhemma', 'puyyma']
['dharshini', 'dhemma', 'puyyma']
```

## Why?

Because `print(student)` prints the entire list every time.

---

# Correct Way

```python
student = ["dharshini", "dhemma", "puyyma"]

for study in student:
    print(study)
```

## Output

```python
dharshini
dhemma
puyyma
```

---

# Example 2: Iteration with Numbers 

```python
numbers = [1, 2, 3, 4]

for num in numbers:
    print(num * 2)
```

## Output

```python
2
4
6
8
```

---

# Example 3: Using `range()`

```python
for i in range(5):
    print(i)
```

## Output

```python
0
1
2
3
4
```

---

# Key Point

A `for` loop in Python is mainly used for iteration.

## Syntax

```python
for variable in list:
    # code
```


**LEN** 

