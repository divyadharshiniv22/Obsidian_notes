Return Values

To make the program interactive, we can ask the user for their name and greet them personally.

```python
name = input("What's your name? ")
print("Hello,", name)
```

### Step-by-step

1. The `input()` function displays the prompt **"What's your name? "**.
    
2. The user types a name and presses Enter.
    
3. The function **returns** the entered text.
    
4. The returned value is stored in the variable `name`.
    
5. The `print()` function uses that variable to display a personalized greeting.
    

### Key Concepts

- **Return value**: Data that a function gives back after finishing its work.
    
- **Variable**: A container used to store that returned value so it can be reused later in the program.

## Variables

A **variable** is a container in computer memory used to store a value such as a number, text, image, or other data. Unlike mathematical variables such as `x` or `y`, programming variables can have meaningful names that describe what they store.

Example:

```
name = input("What's your name? ")
```

Here:

- `name` is the **variable**
    
- The value typed by the user is stored inside the variable
    

If we print the variable:

```
print("Hello,")
print(name)
```

Python prints the **value stored inside the variable**, not the word `"name"`, because the variable is written **without quotes**.

**Output example**

```
Hello,
David
```

This demonstrates that variables allow us to store user input and reuse it later in the program.