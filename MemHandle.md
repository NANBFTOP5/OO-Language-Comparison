# Memory Management

Memory management in both languages is garbage collected. There are differences in implementation but, from a high level they are very similiar.

### Python:
Objects are never explicitly destroyed, however, when they become unreachable they may be garbage-collected. 

Python watches the reference count on objects, and anytime it reaches zero, the object is immediately removed.

python allows some interaction with the garbage collector with

```python 
import gc
```