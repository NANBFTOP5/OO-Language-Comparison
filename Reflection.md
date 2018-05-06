# Reflection

## Python

* What reflection abilities are supported?
    
    A Python script can find out about the type, class, attributes and methods of an object. This is referred to as reflection or introspection.

    ```python
    # Python program to illustrate reflection
    def reverse(seq):
        SeqType = type(seq)
        emptySeq = SeqType()
        
        if seq == emptySeq:
            return emptySeq
        
        restrev = reverse(seq[1:])
        first = seq[0:1]
        
        # Combine the result
        result = restrev + first
        
        return result
    
    # Driver code
    print(reverse([1, 2, 3, 4]))
    print(reverse("HELLO"))

    # Output
    [4,3,2,1]
    OLLEH
    ```

* How is reflection used?
    
    Reflection-enabling functions include type(), isinstance(), callable(), dir() and getattr().

    1. type and isinstance - Refer here
    2. ```Callable()```: A callable means anything that can be called. For an object, determines whether it can be called. A class can be made callable by providing a ```__call__()``` method. The ```callable()``` method returns True if the object passed appears callable. If not, it returns False.

    ```python
    x = 5

    def testFunction():
    print("Test")
    
    y = testFunction

    if (callable(x)):
        print("x is callable")
    else:
        print("x is not callable")

    if (callable(y)):
        print("y is callable")
    else:
        print("y is not callable")
    ```


## C#
* What reflection abilities are supported?

     Reflection provides objects (of type Type) that describe assemblies, modules and types. You can use reflection to dynamically create an instance of a type, bind the type to an existing object, or get the type from an existing object and invoke its methods or access its fields and properties. If you are using attributes in your code, reflection enables you to access them. For more information, see Attributes.

* How is reflection used?

```c#
    // Using GetType to obtain type    information:  
    int i = 42;  
    System.Type type = i.GetType();  
    System.Console.WriteLine(type);  

    //output
    System.Int32
```