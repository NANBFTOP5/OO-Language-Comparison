# Interfaces /  Protocols

## Python

* What does the language support?

    Interfaces is not necessary in Python. This is because Python has proper multiple inheritance, and also ducktyping, which means that the places where you must have interfaces in Java, you don't have to have them in Python.
    ```python
    class IInterface:
    def show(self): raise NotImplementedError

    class MyClass(IInterface):
    def show(self): print "Hello World!"

    ```

* What abilities does it have?

    That said, there is still several uses of interfaces. Some of them are covered by Pythons Abstract Base Classes, introduced in Python 2.6. That's useful if you want to make baseclasses that can not be instantiated, but provide a specific interface or part of an implementation.

* How is it used?

    if you somehow want to specify that an object implements a specific interface, and you can use ABC's for that too by subclassing from them. Another way is zope.interface, a module that is a part of the Zope Component Architecture, a really awesomely cool component framework. Here you don't subclass from the interfaces, but instead mark classes (or even instances) as implementing an interface. This can also be used to look up components from a component registry.

## C#

* What does the language support?
    * Supports interfaces
    ```c#
    interface ISampleInterface
    {
        void SampleMethod();
    }

    ```

* What abilities does it have?
    * a class or interface can implement numberous interfaces

    ```c#
        class ImplementationClass : ISampleInterface
    {
        // Explicit interface member implementation: 
        void ISampleInterface.SampleMethod()
        {
            // Method implementation.
        }

        static void Main()
        {
            // Declare an interface instance.
            ISampleInterface obj = new ImplementationClass();

            // Call the member.
            obj.SampleMethod();
        }
    }
    ```

* How is it used?
    * C# offers the option to use delegates which can often be more powerful than interfaces

