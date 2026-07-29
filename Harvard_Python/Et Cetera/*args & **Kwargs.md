# Difference

|`*args`|`**kwargs`|
|---|---|
|Positional arguments|Keyword (named) arguments|
|Stored as **tuple**|Stored as **dictionary**|
|`f(1,2,3)`|`f(name="Divya", age=22)`|
|Access by index (`args[0]`)|Access by key (`kwargs["name"]`)|

---

# Interview Answer

**Q: What is `*args`?**

`*args` collects any number of positional arguments passed to a function and stores them as a **tuple**.

**Q: What is `**kwargs`?**

`**kwargs` collects any number of keyword (named) arguments passed to a function and stores them as a **dictionary**.

# Program 1 - `*args` (Positional Arguments)

```python

def f(*args, **kwargs):
    print("positional :", args)

f(100, 30, 40)
```
# Why Tuple?

Because Python doesn't know how many positional arguments you'll pass.

# Program 2 - `**kwargs`

```python

def f(*args, **kwargs):
    print("named:", kwargs)

f(dharshini=100, divya=300, gautam=500)
```

# Why Dictionary?

Because keyword arguments always have

```
key = value
```

Example

```python
name="Divya"
age=22
city="Chennai"
```

