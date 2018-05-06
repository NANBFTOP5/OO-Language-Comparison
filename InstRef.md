# Instance reference name in data type (class)

## this? Self?

* Python

    both ```self``` and ```this``` are used for accessing the variables and functions associated with the current instance. the ```self``` variable represents the instance of the object itself. Most object-oriented languages pass this as a hidden parameter to the methods defined on an object; Python does not. You have to declare it explicitly.

    ```python
    class A(object):
	    def __init__(self):
	        self.x = 'Hello'
	
	    def method_a(self, foo):
	        print self.x + ' ' + foo
    ```

* C#

     C# designates use of the this keyword to reference members of instantiated objects from within.

     ```c#
    public class Book
    {
        private string BOOk_Name;
        private string ISBN;

        public Pet(string BOOk_Name, string ISBN)
        {
            this.BOOk_Name = BOOk_Name; // this.BOOk_Name references the current object instance
            this.ISBN = ISBN; // this.ISBN references the current object instance
        }
    }
     ```


