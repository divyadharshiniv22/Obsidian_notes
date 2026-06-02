# Libraries in Python

A **library** is a collection of pre-written code that helps developers perform tasks easily without writing everything from scratch.

---

# Simple Meaning

```
Library = reusable code written by others
```

You import and use it in your program.

---

# Why We Use Libraries

Libraries help to:

- save time
- reduce coding effort
- avoid rewriting common logic
- build powerful applications quickly

---

# Real-Life Analogy

```
Library = toolbox
```

Instead of making tools yourself, you use ready-made tools.

---

# Example Without Library

To calculate square root manually is difficult.

With library:

```
import mathprint(math.sqrt(25))
```

Output:

```
5.0
```

Here:

```
math
```

is a library.

---

# How to Use Libraries

## Step 1 — Import Library

```
import math
```

---

## Step 2 — Use Functions

```
math.sqrt(16)
```

---

# Common Python Libraries

|Library|Purpose|
|---|---|
|`math`|Mathematical operations|
|`random`|Random numbers|
|`datetime`|Date and time|
|`os`|Operating system tasks|
|`json`|JSON handling|
|`pandas`|Data analysis|
|`numpy`|Numerical computing|
|`matplotlib`|Plotting graphs|
|`requests`|API calls|
|`tensorflow`|Machine learning|

---

# Example 1 — Random Library

```
import randomprint(random.randint(1, 10))
```

Generates random number.

---

# Example 2 — Datetime Library

```
import datetimeprint(datetime.datetime.now())
```

Shows current date and time.

---

# Types of Libraries

## 1. Built-in Libraries

Already available in Python.

Examples:

```
mathrandomosdatetime
```

---

## 2. External Libraries

Need installation using:

```
pip install library_name
```

Example:

```
pip install pandas
```

---

# Example Using Pandas

```
import pandas as pd
```

Used heavily in:

- data analysis
- AI/ML
- analytics projects

---

# What is `import`

```
import math
```

means:

```
"Bring math library into this program."
```

---

# Real Job Usage

Libraries are used everywhere:

|Field|Common Libraries|
|---|---|
|Backend|Flask, FastAPI|
|Data Science|pandas, numpy|
|AI/ML|TensorFlow, PyTorch|
|Automation|selenium|
|APIs|requests|
|Visualization|matplotlib|

---

# Important Point

Without libraries:

❌ development becomes slow

With libraries:

✅ faster development  
✅ reusable solutions  
✅ industry-standard code

---

# Short Definition

```
A library is a collection of reusable pre-written code used to perform specific tasks.
```