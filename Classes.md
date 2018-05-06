# Classes

Defining and managing classes in python is very straightforward.
### Python:

```python
	class ClassName:
		def __init__(self, a, b):	#initializer	(fig 1)
			self.a = a
			self.b = b

		def getA(self):			#method		(fig 2)
			return a
	a = 4
	b = 5
	example = ClassName(a,b)		#constructing 	(fig 3)
	print(example.getA) 			#prints 4	(fig 4)

	del example				#destructing	(fig 5)
```
In Python you can decalare 'special' functions by using a double underscore '__'. Special functions are used for a variety of things beyond what normal methods could handle, such as initializers/contructors and de-initializers/destructors.
### C#:

```C#
public class Dog{
    public string name;
    public int age;
    
    public Dog(){	//initializer
        this.name = "Paws";
        this.age = 3;
    }
    
    public dogInfo(string name){	//method
        this.name = name;
        this.age = 3;
		this.dogAge = age * 7;
    }
}
```



## Initializers / Constructors:

### Python:
The `__init__()` is the contructor of a class. This function is executed whenever a new object of that class is created. (fig 1) Contructors can be overloaded.

### C#:
In C# constructors are defined similiarly to a method but with the same name as the class. They similiarly always called when a class instance is created. Contructors can be overloaded.

## Methods: 

### Python:
Methods of a class are simply declared within the class (spaces count in python). (fig 2)
### C#:
In C# methods are defined within a class, they require access modifiers.

## De-Initializers/Destructors:

### Python:
The `__del__()` function is the destructor of a class. This function is executed whenever an instance of the class is about to be destroyed. (fig 5)
### C#:

C# has a garbage collector that will automatically clean instances that are no longer needed.
