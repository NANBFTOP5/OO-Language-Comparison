# Types of OO Languges

## what types does the language support?




## Python

    1. Boolean
        ```python
        bool A = true
        ```
    2. Sequencces
        * string
        
    3. Numeric Types
        * int
        * double
        * float
        * long
        * complex
        ```python

        counter = 100          # An integer assignment
        miles   = 1000.0       # A floating point
        name    = "John"       # A string
        lon     = 123L         # A Long
        aCom    = 34+3J        # A Complex

        ```
    4. Mapping
        * dict
    5. Sets
        * set
        * frozen set
    

## Are both reference and value types supported?

* yes

    ### pass to a method

    ```python
    def try_to_change_list_contents(the_list):
    print('got', the_list)
    the_list.append('four')
    print('changed to', the_list)

    outer_list = ['one', 'two', 'three']

    print('before, outer_list =', outer_list)
    try_to_change_list_contents(outer_list)
    print('after, outer_list =', outer_list)

    Output:
    before, outer_list = ['one', 'two', 'three']
    got ['one', 'two', 'three']
    changed to ['one', 'two', 'three', 'four']
    after, outer_list = ['one', 'two', 'three', 'four']

    ```

## Can new value types be created?

* python uses the NewType() to create distinct Types: 

    ```python

    from typing import NewType

    UserId = NewType('UserId', int)
    some_id = UserId(14203175)
    def get_user_name(user_id: UserId) -> str:
        ...

    # typechecks
    user_a = get_user_name(UserId(123456))

    # does not typecheck; an int is not a UserId
    user_b = get_user_name(-1)
    # 'output' is of type 'int', not 'UserId'
    output = UserId(14203175) + UserId(123456)
    ```

## C#

## What types does the language support?
1. bool

2. char

3. double

4. float

5. int

6. long
7. unit
8. object
9. string
10. byte
11. decimal

    ```c#
        int a = 5;             
        bool test = true;
        float temperature;
        string name;
        MyClass myClass;
        char firstLetter = 'C';
        var limit = 3;
        int[] source = { 0, 1, 2, 3, 4, 5 };
        var query = from item in source
                    where item <= limit
                    select item;
    ```

## Are both reference and value types supported?
* Yes

## Can new value types be created?
* yes

```c#
public struct Book  
{  
    public decimal price;  
    public string title;  
    public string author;  
}  
```
