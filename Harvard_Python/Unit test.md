Yes. **pytest** is the most popular Python testing framework and the one I recommend you learn first.

### What is pytest?

It is a tool that automatically runs your test cases and tells you whether they pass or fail.

### Example

#### calculator.py

```
def add(a, b):    return a + b
```

#### test_calculator.py

```
from calculator import adddef test_add():    assert add(2, 3) == 5
```

### Run the test

Open a terminal:

```
pytest
```

Output:

```
==================1 passed==================
```

---

## Structure of a pytest test

```
def test_function_name():    assert actual_result == expected_result
```

Example:

```
def test_add():    assert add(10, 20) == 30
```

---

## Multiple Test Cases

```
from calculator import add

def test_add_positive():    
assert add(2, 3) == 5

def test_add_negative():    
assert add(-2, -3) == -5

def test_add_zero():    
assert add(5, 0) == 5
```

## Rules to Remember

1. Test file name should start with `test_`

```
test_calculator.py
```

2. Test function name should start with `test_`

```
def test_add():
```

3. Use `assert`

```
assert add(2, 3) == 5
```

4. Run all tests with:

```
pytest
```

---

### Practice Exercise

Create:

```
# calculator.pydef multiply(a, b):    return a * b
```

Now write three pytest test cases:

```python

from calculator import multiply

def test_multiply_positive():    
   assert multiply ([3 ,2]) == 6

def test_multiply_zero():    
   assert multiply ([3,0]) == 0

def test_multiply_negative():      assert multiply ([-3,4]) == -12
```