  
![[Pasted image 20260708185112.png]]
```python
class animal(): 
     def __init__(self, name): 
        self.name = name
class dog(animal):
     def __init__(self, name, age):
        super().__init__(name) 
        self.age = age 
d = dog("mani", 12)
```


```python
dog("mani",12) 
     ↓
Dog.__init__()
     ↓   
super().__init__(name) 
     ↓ 
Animal.__init__() 
     ↓ 
self.name = "mani" 
     ↓
Return to Dog.__init__()
     ↓ 
self.age = 12
```
When I create `dog("mani", 12)`, Python first calls the `Dog` constructor. Inside it, `super().__init__(name)` calls the parent class (`Animal`) constructor to initialize the `name` attribute. After the parent constructor finishes, control returns to the `Dog` constructor, which initializes the `age` attribute. Finally, the object contains `name = "mani"` and `age = 12`.
```python


  

class father():

  def work(self):

       print("he works well")

class mother():

  def cook(self):

       print("she cooks well")

class child(father,mother):

      pass

c = child()

c.work()

c.cook()
```

  

## Step 1

```PYTHON
class father():
```

Python creates a class named `father`.

It contains one method:

```python
def work(self):
```

Nothing is printed yet.

---

## Step 2

```python
class mother():
```

Python creates another class named `mother`.

It contains one method:

```python
def cook(self):
```

Nothing is printed yet.

---

## Step 3

```python
class child(father, mother):
    pass
```

Python creates the `child` class.

It says:

```python
Child inherits from Father and Mother.
```

Now `child` has access to:

- `work()` from `father`
- `cook()` from `mother`

---

## Step 4

```python
c = child()
```

Python creates an object.

```python
c
│
▼
Child Object
```

Nothing is printed yet.

---

## Step 5

```python
c.work()
```

Python looks for `work()`.

### Search process

```python
Child
│
├── work() ❌ Not found
│
▼
Father
│
├── work() ✅ Found
```

Python then **internally changes**:

```python
c.work()
```

to:

```python
father.work(c)
```

So:

```python
self = c
```

Now Python executes:

```python
print("he works well")
```

Output:

```python
he works well
```

---

## Step 6

```python
c.cook()
```

Python looks for `cook()`.

### Search process

```python
Child
│
├── cook() ❌ Not found
│
▼
Father
│
├── cook() ❌ Not found
│
▼
Mother
│
├── cook() ✅ Found
```

Python internally changes:

```
c.cook()
```

to:

```
mother.cook(c)
```

So:

```
self = c
```

Now Python executes:

```
print("she cooks well")
```

Output:

```
she cooks well
```

---

# Final Output

```
he works well
she cooks well
```