# Comparisons

## Python

* In Python comparisons yield boolean values: `True` and `False`
* Comparisons can be combined `a < b <= c == a < b and b <= c` arbitrarily
* Python compares the values of objects
* Compared objects do not need to have the same type, if both are numbers they are converted to a common type. Otherwise objects of different types always compare unequal, and are ordered consistently but not arbitrarily.

```python

x = 1
y = '1'

z = (x == y) 
print(x) #true
```

# C#

In C# there are two ways to compare objects, `==` and the method `.Equals`. If `==` is used the values or objects must be of the same type, otherwise you may get an exception.

```C#
string a = new string(new char[] {'a', 'b', 'c', 'd', 'e'});
string b = new string(new char[] {'a', 'b', 'c', 'd', 'e'});

a.Equals(b); #true
```
