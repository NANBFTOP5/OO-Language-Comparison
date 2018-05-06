# Lambda expressions, closures, or functions as types

 ## python

 * The lambda operator or lambda function is a way to create small anonymous functions, i.e. functions without a name. These functions are throw-away functions, i.e. they are just needed where they have been created. Lambda functions are mainly used in combination with the functions filter(), map() and reduce(). The lambda feature was added to Python due to the demand from Lisp programmers. 

 * A closure is a function object that remembers values in enclosing scopes regardless of whether those scopes are still present in memory.
    * The map() Function

        ```Python
        r = map(func, seq)


        def fahrenheit(T):
        return ((float(9)/5)*T + 32)

        def celsius(T):
            return (float(5)/9)*(T-32)
        temp = (36.5, 37, 37.5,39)

        F = map(fahrenheit, temp)
        C = map(celsius, F)

        >>> a = [1,2,3,4]
        >>> b = [17,12,11,10]
        >>> c = [-1,-4,5,9]
        >>> map(lambda x,y:x+y, a,b)
        [18, 14, 14, 14]
        >>> map(lambda x,y,z:x+y+z, a,b,c)
        [17, 10, 19, 23]
        >>> map(lambda x,y,z:x+y-z, a,b,c)
        [19, 18, 9, 5]

        ```

## C#

* A lambda expression is an anonymous function that you can use to create delegates or expression tree types. By using lambda expressions, you can write local functions that can be passed as arguments or returned as the value of function calls. Lambda expressions are particularly helpful for writing LINQ query expressions.

* To create a lambda expression, you specify input parameters (if any) on the left side of the lambda operator =>, and you put the expression or statement block on the other side. For example, the lambda expression x => x * x specifies a parameter that’s named x and returns the value of x squared. You can assign this expression to a delegate type, as the following example shows:

    ```c#
    delegate int del(int i);  
    static void Main(string[] args)  
    {  
        del myDelegate = x => x * x;  
        int j = myDelegate(5); //j = 25  
    }
    //To create an expression tree type:
    using System.Linq.Expressions;  

    namespace ConsoleApplication1  
    {  
        class Program  
        {  
            static void Main(string[] args)  
            {  
                Expression<del> myET = x => x * x;  
            }  
        }  
    }

    ```