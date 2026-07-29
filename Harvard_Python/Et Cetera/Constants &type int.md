
* Some languages allow you to create variables that are unchangeable, called “constants”.
* ```python 
  MEOWS = 3

for _ in range(MEOWS):

print("MEOWS")

  
   ```
  if you writing in capital letter means .....it's importance so don't change it .


## Type Hints and mypy (தமிழில்)

Type Hints மற்றும் **mypy** இரண்டும் Python code-ஐ **பிழைகள் (errors) வருவதற்கு முன்பே கண்டுபிடிக்க** உதவுகின்றன.

---

# 1. Type Hint என்றால் என்ன?

**Type Hint** என்பது ஒரு variable அல்லது function எந்த data type-ஐ பயன்படுத்த வேண்டும் என்று எழுதும் **குறிப்பு (hint)**.

உதாரணம்:

```
name: str = "Divya"
age: int = 22
height: float = 5.4
is_student: bool = True
```

**DOCSTRING**

```PYTHON
def meow(n):
    """
    Meow n times.

    :param n: Number of times to meow
    :type n: int
    :raise TypeError: If n is not an int
    :return: A string of n meows, one per line
    :rtype: str
    """
    return "meow\n" * n


number = int(input("Number: "))
meows = meow(number)
print(meows, end="")

```