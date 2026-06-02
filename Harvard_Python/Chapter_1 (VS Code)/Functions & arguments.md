  # 🔧 Functions in Programming (Obsidian Notes)

## 🔹 What is a Function?

- In almost **every programming language**, we have access to **functions**
    
- A **function** is like an **action** or a **verb**
    
- It allows us to **do something** in a program
    

👉 Think of a function as a **command** that tells the computer to perform a task

---

## 🔹 Built-in (Predefined) Functions

- Most programming languages come with a **predefined set of functions**
    
- These are **basic actions** that the computer already knows how to perform
    
- The language itself understands how to execute these functions
    

Examples of basic actions:

- Display text
    
- Take input
    
- Perform calculations

**Bulit-in Function Example like (when already built in computer eg : print(), count(), input(),max(),min())   user defined function means write own code like hello world, ect....**


---

## 🔹 Example in Python

### File name:

`hello.py`

### Code:

`print("hello world")`

### Explanation:

- `print()` is a **built-in function**
    
- Its job is to **display output** on the screen
    
- `"hello world"` is the **data** passed to the function
    
- When the program runs, the interpreter executes this function
    

---

## 🔹 Why Functions are Important

- They make code **reusable**
    
- They make programs **easier to read**
    
- They reduce repetition
    
- They allow complex tasks to be done in a **single line**
    

---

## 🔹 Real-Life Example

🧠 **Function = Verb**

Just like:

- _eat_
    
- _run_
    
- _write_
    

In programming:

- `print()` → display
    
- `input()` → get input
    
- `len()` → count length
    

---

## ✍️ One-Line Definition (Exam Ready)

> **A function is a reusable block of code that performs a specific action in a program.**


## ARGUMENTS

** ( ) - parentheses.
**(1,2,3 ) - arguments 

**Definition**  
An **argument** is an input to a function that influences its behavior.

When Python developers created functions such as `print()`, they designed them to accept inputs inside parentheses. These inputs can be any string of text—English or any other language—that we want the function to display on the screen.

For example:

```
print("Hello, World")
```

Here, `"Hello, World"` is the **argument** passed to the `print()` function.

---

## Side Effects

What is the program doing on the screen?

It is **printing**, meaning it is displaying text visually. In programming, this kind of outcome is called a **side effect**.

A **side effect** is any observable action performed by a function besides returning a value.  
Side effects can include:

- Displaying text on the screen (visual)
    
- Playing sound (audio)
    
- Writing data to a file
    
- Sending data over a network
    

In this case, the function `print()`produces a side effect by showing the words **"Hello, World"** on the screen.