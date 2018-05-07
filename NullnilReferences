#  Null/nil references

## Python

* In Python, None is distinct from any other value and used throughout the language and library to indicate the absence of a “real” value.

* Many would argue that the word "null" is somewhat esoteric. It's not exactly the most friendliest word to programming novices. Also, "None" refers exactly to the intended functionality - it is nothing, and has no behaviour.

* In most object-oriented languages, the naming of objects tend to use camel-case syntax. eg. ThisIsMyObject. As you'll see soon, Python's None type is an object, and behaves as one.

    ```python
    if null_variable is None:
        print('null_variable is None')
    else:
        print('null_variable is not None')

    if not_null_variable is None:
        print('not_null_variable is None')
    else:
        print('not_null_variable is not None')


    # The == operator
    if null_variable == None:
        print('null_variable is None')
    else:
        print('null_variable is not None')

    if not_null_variable == None:
        print('not_null_variable is None')
    else:
        print('not_null_variable is not None')

    ```

## C#

* In C#, null is a value of any object type. Any attempt to access a field or method of null triggers an exception. "The null keyword is a literal that represents a null reference, one that does not refer to any object. null is the default value of reference-type variables. Ordinary value types cannot be null. However, C# 2.0 introduced nullable value types. See Nullable Types." 

* Nullable Types are instances of System. Nullable and add the feature of being able to be set to null in addition to the usual type, hence the name Nullable. This helps with working with data that may not be there, i.e. databases where some values are not set.



    ```c#
    using System;
    
    class NullableExample
    {
      static void Main()
      {
          int? num = null;

          // Is the HasValue property true?
          if (num.HasValue)
          {
              Console.WriteLine("num = " + num.Value);
          }
          else
          {
              Console.WriteLine("num = Null");
          }

          // y is set to zero
          int y = num.GetValueOrDefault();

          // num.Value throws an InvalidOperationException if num.HasValue is false
          try
          {
              y = num.Value;
          }
          catch (InvalidOperationException e)
          {
             Console.WriteLine(e.Message);
          }
       }
    }
    // The example displays the following output:
    //       num = Null
    //       Nullable object must have a value.
    ```
