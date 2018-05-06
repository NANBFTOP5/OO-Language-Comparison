# Singleton

## Python

* How is a singleton implemented?
    * Possibly the simplest design pattern is the singleton, which is a way to provide one and only one object of a particular type. To accomplish this, you must take control of object creation out of the hands of the programmer. One convenient way to do this is to delegate to a single instance of a private nested inner class:

    ```python
    # Singleton/SingletonPattern.py

    class OnlyOne:
        class __OnlyOne:
            def __init__(self, arg):
                self.val = arg
            def __str__(self):
                return repr(self) + self.val
        instance = None
        def __init__(self, arg):
            if not OnlyOne.instance:
                OnlyOne.instance = OnlyOne.__OnlyOne(arg)
            else:
                OnlyOne.instance.val = arg
        def __getattr__(self, name):
            return getattr(self.instance, name)

    x = OnlyOne('sausage')
    print(x)
    y = OnlyOne('eggs')
    print(y)
    z = OnlyOne('spam')
    print(z)
    print(x)
    print(y)
    print(`x`)
    print(`y`)
    print(`z`)
    output = '''
    <__main__.__OnlyOne instance at 0076B7AC>sausage
    <__main__.__OnlyOne instance at 0076B7AC>eggs
    <__main__.__OnlyOne instance at 0076B7AC>spam
    <__main__.__OnlyOne instance at 0076B7AC>spam
    <__main__.__OnlyOne instance at 0076B7AC>spam
    <__main__.OnlyOne instance at 0076C54C>
    <__main__.OnlyOne instance at 0076DAAC>
    <__main__.OnlyOne instance at 0076AA3C>
    '''
    ```
* Can it be made thread-safe?

    Singleton could be thread safe in Python by manipulate thread before using singleton object such as lock the thread.
* Can the singleton instance be lazily instantiated?

    The singleton instance could be lazily instantiated in Python.

    Lazy instantiation makes sure that the object gets created when it's actually needed. Consider lazy instantiation as the way to work with reduced resources and create them only when needed.

    ## C#

* How is a singleton implemented?

    The following implementation of the Singleton design pattern follows the solution presented in Design Patterns: Elements of Reusable Object-Oriented Software [Gamma95] but modifies it to take advantage of language features available in C#, such as properties:
    ```c#
    using System;

    public class Singleton
    {
    private static Singleton instance;

    private Singleton() {}

    public static Singleton Instance
    {
        get 
        {
            if (instance == null)
            {
                instance = new Singleton();
            }
            return instance;
        }
    }
    }
    ```
* Can it be made thread-safe?

    NO. The main disadvantage of this implementation, however, is that it is not safe for multithreaded environments. If separate threads of execution enter the Instance property method at the same time, more that one instance of the Singleton object may be created. Each thread could execute the following statement and decide that a new instance has to be created

* Can the singleton instance be lazily instantiated?

    Because the Singleton instance is referenced by a private static member variable, the instantiation does not occur until the class is first referenced by a call to the Instance property. This solution therefore implements a form of the lazy instantiation property, as in the Design Patterns form of Singleton.