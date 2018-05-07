# Inheritance
## Python
* Supports Inheritance
* Supports multiple Inheritance
```python
class SuperHeroDog(Dog,SuperHero):  #methods in SuperHeroDog have precidence, then Dog, then SuperHero in that order.
                                    #Diamond problem solved by dynamic ordering which solves the identicle parent problem.
    __init():
        
```

# C#
    * Supports Inheritance
    * Does not support multiple Inheritance
    * Classes do not inherit from object by default, (inheritance forest)
```C#
public class Dog : Pet {
}