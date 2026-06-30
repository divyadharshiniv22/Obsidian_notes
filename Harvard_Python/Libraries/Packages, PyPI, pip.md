# Packages in Python

A **package** is a collection of modules organized inside folders.

---

# Simple Meaning

```
Package = folder containing multiple Python modules
```

---

# Structure Example

```
project/│
├── math_tools/│     
       ├── add.py│     
       ├── sub.py│     
       └── mul.py
```

Here:

```
math_tools
```

is a package.

Files inside are modules.

---

# Why We Use Packages

Packages help to:

- organize large projects
- group related modules
- avoid naming conflicts
- make code reusable

---

# Real-Life Analogy

```
Package = folderModule = file inside folder
```

---

# Example Import

```
from math_tools import add
```

---

# PyPI (Python Package Index)

PyPI is the official website/repository for Python packages.

---

# Simple Meaning

```
PyPI = online storehouse of Python packages
```

Developers upload packages there.

---

# Official Website

[PyPI](https://pypi.org?utm_source=chatgpt.com)

---

# Examples of Packages on PyPI

| Package      | Purpose             |
| ------------ | ------------------- |
| `numpy`      | Numerical computing |
| `pandas`     | Data analysis       |
| `flask`      | Web development     |
| `tensorflow` | Machine learning    |
| `requests`   | API calls           |

---

# pip in Python

`pip` is Python’s package manager.

Used to install packages from PyPI.

---

# Simple Meaning

```
pip = tool used to install Python packages
```

---

# Install Package

```
pip install pandas
```

---

# What Happens

`pip`:

- connects to PyPI
- downloads package
- installs it into Python environment

---

# Example

```
pip install numpy
```

Then use in Python:

```
import numpy
```

---

# Check Installed Packages

```
pip list
```

---

# Upgrade Package

```
pip install --upgrade pandas
```

---

# Uninstall Package

```
pip uninstall pandas
```

---

# Relationship Between Package, PyPI, and pip

```
PyPI → stores package
pip  → installs packagespackage → reusable code
```

---

# Real Job Usage

Used everywhere in professional development:

| Field        | Common Packages     |
| ------------ | ------------------- |
| Backend      | Flask, Django       |
| AI/ML        | TensorFlow, PyTorch |
| Data Science | pandas, numpy       |
| APIs         | requests            |
| Automation   | selenium            |

---

# Example Workflow

## Install package

```
pip install requests
```

---

## Use package

```
import requests
```

---

# Important Point

Without `pip`, installing libraries manually would be difficult.

`pip` automates package management.

---

# Difference Between Module, Package, and Library

| Term    | Meaning                        |
| ------- | ------------------------------ |
| Module  | Single `.py` file              |
| Package | Collection of modules          |
| Library | Collection of packages/modules |

---

# Short Definitions

```
Package → collection of modules
```

```
PyPI → official repository of Python packages
```

```
pip → tool used to install Python packages
```