# Name Spaces

## How are name spaces implemented? How are the name spaces implemented?

* Python

    A namespace is a mapping from names to objects. Most namespaces are currently implemented as Python dictionaries, but that’s normally not noticeable in any way (except for performance), and it may change in the future. Examples of namespaces are: the set of built-in names (containing functions such as abs(), and built-in exception names); the global names in a module; and the local names in a function invocation. In a sense the set of attributes of an object also form a namespace.

    ```
    >>> import math
    >>> dir(math)
    ['__doc__', '__file__', '__name__', '__package__', 'acos', 'acosh', 'asin',
    'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh',
    'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor',
    'fmod', 'frexp', 'fsum', 'gamma', 'hypot', 'isinf', 'isnan', 'ldexp',
    'lgamma', 'log', 'log10', 'log1p', 'modf', 'pi', 'pow', 'radians', 'sin',
    'sinh', 'sqrt', 'tan', 'tanh', 'trunc']


    def scope_test():
    def do_local():
        dog = "local dog"

    def do_nonlocal():
        nonlocal dog
        dog = "nonlocal dog"

    def do_global():
        global dog
        dog = "global dog"

    spam = "test dog"
    do_local()
    print("After local assignment:", dog)
    do_nonlocal()
    print("After nonlocal assignment:", dog)
    do_global()
    print("After global assignment:", dog)


    ```

* C#

    organize classes

    declaring your own namespaces can help you control the scope of class and method names in larger programming projects

    ```
    using System;
    ```

    the 'using keyword' allows acess to system and all of its deravitives such as 'Console' so the programmer doesnt have to delcare System.Console every time he wishes to use a method found in System.Console. The '.' is used to delimit namespaces.

    ```
    namespace SampleNamespace
    {
        class SampleClass
        {
           public void SampleMethod()
          {
             System.Console.WriteLine(
                "SampleMethod inside SampleNamespace");
            }
     }
    }

    ```