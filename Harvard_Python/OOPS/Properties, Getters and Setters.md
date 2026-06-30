
 ### Property (`@property`) — Simple Explanation

A **property** lets you use a method like a normal variable.

### Memory Trick

```python
Getter = Get data
Setter = Set/Update data
Property = Makes getter/setter look like normal variables
```

Example:

```python
student.name      # Getter runs
student.name = "Divya"  #Setter runs or update 
```

Without property:

```python

class Student:   
def get_name(self):        return "Divya"
student = Student()
print(student.get_name())
```

Output:

```python
Divya
```

You have to call a method:

```python
student.get_name()
```

---

### With Property

```python
class Student:    
@property    
def name(self):        
return "Divya"
student = Student()
print(student.name)
```

Output:

```python
Divya
```

Notice:

```python
student.name
```

looks like a variable, but Python is actually calling the method behind the scenes.

---

### Why Use Property?

Suppose today you have:

```python
student.name
```

Later you want to add validation or extra logic.

With `@property`, you can change the internal implementation without changing how other code uses it.

Users still write:

```python
student.name
```

---

### Easy Memory Trick

```python
Normal Method:
student.get_name()
Property:
student.name
```

A **property** makes a method behave like an attribute (variable).

### Interview Answer

> A property is a special method accessed like an attribute. It allows controlled access to an object's data while keeping the syntax simple and readable.