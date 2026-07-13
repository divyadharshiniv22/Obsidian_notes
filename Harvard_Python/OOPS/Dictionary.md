A **dictionary** is a data structure that stores data in **key-value pairs**.

```python

student = {    
            "name": "Divya",                           "house": "Chennai"
 }
```

### Interview Answer

```python
### Interview Answer

> A dictionary is a collection of key-value pairs. Each value is accessed using its key instead of an index. Dictionaries are mutable, meaning items can be added, updated, or removed.
```

```python
def main():
    student = get_student()
    print(f"{student['name']} from{student['house']}")

def get_student():
    student = {}
    student["name"]= input("name :")
    student["house"]= input("house:")
    return student

if __name__ == "__main__":
    main()
```








```python
if __name__ == "__main__"
- current_file_name_assigned_by_python == "__main__".next  is call main() function. check the second line call the get_student() function. see 6 line . student = {} empty it will assigne the student value. 
  
  input is the in build function value assign in the name variable.
  
  input is the in build function value assign in the house variable.

return student the dictionary

 in 2 line return dictionary value assign in the student variable
 
 and print the formatted string dictionary keys 
```

![[Pasted image 20260622125852.png]]