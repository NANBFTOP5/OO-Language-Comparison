# Multithreading

## Python
Multithreading in python is very straightforward.

using the `import Pool` library and the map function, jobs can be split into multiple processes that are computed seperately, then returned back to the main program.

```python

results = []
for item in my_array:
    results.append(my_function(item))
```

can be quickly morphed into 

```python 

from multiprocessing.dummy import Pool as ThreadPool 
pool = ThreadPool(4) 
results = pool.map(my_function, my_array)
```
which will map each function to each array value seperately in threads.
## C#

C# allows you to parallelize loops using the Parallel Class.

```C#
using System.Threading.Tasks;   
class Test
{
    static int N = 1000;

    static void TestMethod()
    {
        // Using a named method.
        Parallel.For(0, N, Method2);

        // Using an anonymous method.
        Parallel.For(0, N, delegate(int i)
        {
            // Do Work.
        });

        // Using a lambda expression.
        Parallel.For(0, N, i =>
        {
            // Do Work.
        });
    }

    static void Method2(int i)
    {
        // Do work.
    }
}
```
This will allocate each iteration of the loop to a seperate thread.