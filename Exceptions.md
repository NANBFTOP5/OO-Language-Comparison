# Errors and Exception Handling

## Python
* Python supports the try-catch method of exception handling.

`except` catches specific exceptions, and allows you to deal with them, all exceptions inherit from the `BaseException` class.

```python
x = 1
y = 0
z = 1
try:
  z = x / y
except ZeroDivisionError:
  z = 0
  print("exception caught")
```
## C#

* C# supports try-catch statements.

```C#
try {
    z = 1/0;
}
catch (exception e){
    z = 0;
}
finally {
    Console.WriteLine("no more exceptions");
}
```