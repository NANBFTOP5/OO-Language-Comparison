Defining classes in python is very straightforward.

Simply:

```python
	class ClassName:
		def __init__(self, a, b):	#initializer (fig 1)
			self.a = a
			self.b = b

		def getA(self):				#method		(fig 2)
			return a
	a = 4
	b = 5
	example = ClassName(a,b)	#constructing 	(fig 3)
	print(example.getA) 		#prints 4		(fig 4)

	del example			#destructing			(fig 5)
```



In Python you can decalare 'special' functions by using a double underscore '__'. Special functions are used for a variety of things beyond what normal methods could handle, such as initializers/contructors and de-initializers/destructors.

Initializers / Constructors:

The `__init__()` is the contructor of a class. This function is executed whenever a new object of that class is created. (fig 1)

Methods: 

Methods of a class are simply declared within the class (spaces count in python). (fig 2)

De-Initializers/Destructors:

The `__del__()` function is the destructor of a class. This function is executed whenever an instance of the class is about to be destroyed. (fig 5)