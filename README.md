Underscore
==========
Obfuscating code by changing the variable names to underscores

## Installation
```
pip install underscore
```

## Usage
```
$ _ file.py > _file.py
```
You can also compile through python
```python
from underscore import _

_(filename, output_filename)
```

## Example

###### Input
```python
# fib.py

from operator import add

def fib(n):
    a, b = 0, 1
    for i in xrange(n):
        a, b = b, add(a, b)
    return b

print fib(10)
```

###### Output
```python
# _fib.py

from operator import add as _

def __(___):
    (____, _____) = (0, 1)
    for ______ in xrange(___):
        (____, _____) = (_____, _(____, _____))
    return _____
print __(10)
```

## Tests
```
nosetests
```
