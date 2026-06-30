```
from random import shuffle
```

| Part      | Meaning            |
| --------- | ------------------ |
| `from`    | take from          |
| `random`  | module             |
| `import`  | bring into program |
| `shuffle` | function           |

---

# Meaning of Full Statement

```
from random import shuffle
```

means:

> “From the `random` module, import the `shuffle` function.”

---

# Example

```
from random import shufflecards = [1, 2, 3, 4]shuffle(cards)print(cards)
```

Possible Output:

```
[3, 1, 4, 2]
```

---

# Important Understanding

## Module

A module contains functions.

Example:

```
random
```

is a module.

---

## Functions Inside `random`

Examples:

```
randint()shuffle()choice()random()
```

These are functions inside the `random` module.

---

# Real Structure

```
random  → module   ↓shuffle → function
```

---

# Similar Example

```
from math import sqrt
```

|Part|Meaning|
|---|---|
|`math`|module|
|`sqrt`|function|

---

# Short Correct Statement

```
from → keywordrandom → moduleimport → keywordshuffle → function
```