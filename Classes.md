Defining classes in python is very straightforward.

Simply:

```
	class ClassName:
		def __init__(self, a, b): #initializer
			self.a = a
			self.b = b

		def getA(self):		#method
			return a
	a = 4
	b = 5
	example = ClassName(a,b)	#constructing
	print(example.getA) 		#prints 4

	del example			#destructing
```



