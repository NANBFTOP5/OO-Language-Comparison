#  Procedural Programming

## Python

* Python supports procedural programming. 

* The procedural style relies on procedure calls to create modularized code. It seeks to simplify the application code by creating small pieces that a developer can view easily. Even though the procedural coding style is an older form of application development, it’s still a viable approach when a task lends itself to step-by-step execution. Here’s an example of the procedural coding style in Python:

    ```python
      def Add(MyList):
          Sum = 0
          if type(MyList) is list:
              for X in MyList:
                  Sum += X
          return Sum
      MyList = [5, 4, 3, 2, 1]
      print(Add(MyList))
    ```
*  The use of a function, Add(), simplifies the overall code in this case. The execution is still systematic, but the code is easier to understand because it’s broken into chunks.

## C#

* C# supports procedural programming. Show a case.

    ```c#
    program Fibonacci;
    function fib(n: Integer): Integer;
    var a: Integer = 1;
        b: Integer = 1;
        f: Integer;
        i: Integer;
    begin
      if (n = 1) or (n = 2) then
         fib := 1
      else
        begin
          for i := 3 to n do
          begin
             f := a + b;
             b := a;
             a := f;
          end;
          fib := f;
        end;
    end;

    begin
      WriteLn(fib(8));
    end.
    ```
