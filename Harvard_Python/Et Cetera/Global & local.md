global variable will work outside the function. local variable will inner function everywhere we want to work we can use global key word.

```python
# a = 10 # global

# b = 4

def greek():

a = 10 # local

b = 4

x=a+b

print(x)

greek()
```


without global it will shows unbound error. so we can use global key words
![[Pasted image 20260724232422.png]]with global key word
![[Pasted image 20260724233411.png]]