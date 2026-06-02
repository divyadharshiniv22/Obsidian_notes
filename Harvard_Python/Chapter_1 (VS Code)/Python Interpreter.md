# 🐍 Python Interpreter – Terminal Execution (Obsidian Notes)

## 🔹 Opening VS Code from Terminal

- Open command prompt **Terminal**
    
- Type:
    
    `code`
    
-a This commnd opens **Visual Studio Code**
    
### Open a specific file in VS Code

`code filename.py`

➡️ VS Code opens the **exact file**

---
## 🔹 Writing Python Code

Create a Python file, for example:

`print("hello world!")`

Save it as:

`hello.py`

---
## 🔹 Running Python Code in Terminal

### On **Windows**

`python hello.py`

### On **Linux / macOS**

`python3 hello.py`

---
## 🔹 What is the Python Interpreter?

- The **Python interpreter** runs Python programs
    
- It executes code **from top to bottom**
    
- It reads code **from left to right**
    
- It executes **line by line**
    

Example:

`print("Hello") print("World")`

➡️ Output appears in the same order

---
## 🔹 How the Interpreter Works

- Computers **do not understand Python**
    
- Computers only understand **binary (0s and 1s)**
    
- The Python interpreter:
    
    - Reads the code **top to bottom**
        
    - Reads each line **left to right**
        
    - Translates Python code into **binary instructions**
        
    - Sends those instructions to the computer
        

---
## 🔹 Running via Interpreter Command

When you type:

`python hello.py`

What happens:

1. Python interpreter opens `hello.py`
    
2. Reads code line by line
    
3. Converts it into machine-understandable form (binary)
    
4. Executes it
    
5. Displays output in terminal
    

---
## 🔹 Key Points to Remember

- Python is an **interpreted language**
    
- No separate compilation step
    
- Errors stop execution immediately
    
- Execution is **sequential**
    

---
## ✍️ One-Line Definition (Exam Ready)

> **The Python interpreter reads Python code line by line and converts it into binary instructions that the computer can understand and execute.**