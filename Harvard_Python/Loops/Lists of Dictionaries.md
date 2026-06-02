# List in Dictionary in Python

## Definition

A list inside a dictionary means:

> a dictionary value can store multiple items using a list.

---

# Structure

```
dictionary = {    "key": [value1, value2, value3]}
```

---

# Simple Example

```
student = {    "name": "Divya",    "skills": ["Python", "SQL", "Pandas"]}
```

---

# Structure Breakdown

|Key|Value|
|---|---|
|`"name"`|`"Divya"`|
|`"skills"`|List of skills|

---

# Visualization

```
student = {    "name": "Divya",    "skills": ["Python", "SQL", "Pandas"]}
```

```
"name"   -> "Divya""skills" -> ["Python", "SQL", "Pandas"]
```

---

# Access List from Dictionary

```
print(student["skills"])
```

### Output

```
['Python', 'SQL', 'Pandas']
```

---

# Access Specific Item in List

```
print(student["skills"][0])
```

### Output

```
Python
```

---

# Loop Through List Inside Dictionary

```
for skill in student["skills"]:    print(skill)
```

### Output

```
PythonSQLPandas
```

---

# Real-Life Example

## Employee Skills

```
employee = {    "name": "Divya",    "skills": ["Python", "Java", "AWS"],    "projects": ["AI Bot", "Web Scraper"]}
```

---

# Access Projects

```
print(employee["projects"])
```

---

# Loop Through Projects

```
for project in employee["projects"]:    print(project)
```

### Output

```
AI BotWeb Scraper
```

---

# Why Use List Inside Dictionary?

Used when:

- one key needs multiple values
- storing grouped data
- handling JSON/API data
