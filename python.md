# Topics to understand

- [x] Context managers `__enter__` and `__exit__`
- [ ] decorators
    - [x] first-class citizens
    - [x] inner/nested functions behaviour
    - [x] higher order functions
    - [ ] understand the OOP's design pattern `decorator pattern` in JAVA
    - [ ] closures and closures factories
    - [ ] namespaces and scope in python
    - [ ] understand flask decorators
    **if you understod this so you understood decorators**
    ```py
    def integer_validator(param_name):
        def decorator(func):
            def wrapper(*args, **kwargs):
                try:
                    param_value = kwargs.get(param_name)
                    if not param_value.isdigit():
                        return jsonify({'error': f'Invalid {param_name}'}), 400
                    return func(*args, **{param_name: int(param_value)})
                except Exception as e:
                    return jsonify({'error': str(e)}), 500

            return wrapper
        return decorator
    
    ```
    

- [ ] classmethod
- [ ] `typing` module
- [ ] static method
- [ ] @property
- [ ] @namesetter
- [ ] yield
- [ ] generators
- [ ] map,filter,reduce,enumerate,zip,counter, ...
- [ ] lambda functions
- [ ] advanced list comperhension
- [ ] iterators
- [ ] why there is no overloading in python
- [ ] dunder methods, know them all
- [ ] metaclasses
- [ ] descriptors
- [ ] dependency intection and inversion of control
- [ ] ABC module, `@abstractmethod`
- [ ] `logging` module
- [ ] async python
- [ ] mutabilty and immutability in python
- [x] `args` and `**kwargs`
- [ ] how this syntax is possble
```python
    "DIRS": [BASE_DIR / "templates"],
```
- [ ]  `late binding` vs `Duck typing`
- [ ] `functools` module
- [ ] `global` and `nonlocal`
- [ ] `globals()` in python
- [ ] object introspection
- [ ] `timeit` module
- [ ] advanced usage of f-string and f-string flags
- [ ] factory methods 

```python
@classmethod
def unit_circle(cls):
    """Factory method creating a circle with radius 1"""
    return cls(1)
```
- [ ] Deeply understand python's OOP
```py
class Circle:
    def __init__(self, radius):
        self.radius = radius

    # mutable property
    @property
    def radius(self):
        """Get value of radius"""
        return self._radius

    @radius.setter
    def radius(self, value):
        """Set radius, raise error if negative"""
        if value >= 0:
            self._radius = value
        else:
            raise ValueError("radius must be non-negative")

    # immutable property
    @property
    def area(self):
        """Calculate area inside circle"""
        return self.pi() * self.radius**2

    # regular method
    def cylinder_volume(self, height):
        """Calculate volume of cylinder with circle as base"""
        return self.area * height

    # class method
    @classmethod
    def unit_circle(cls):
        """Factory method creating a circle with radius 1"""
        return cls(1)

    # static methods
    @staticmethod
    def pi():
        """Value of π, could use math.pi instead though"""
        return 3.1415926535
```
- [ ] `dataclasses` module in python
- how this syntax is possible
```py
from dataclasses import dataclass

@dataclass
class PlayingCard:
    rank: str
    suit: str
```
- [ ] class decorators, how classes are presented in memory and how they're decorated!!
- [ ] `any()` in python







_______________________________________________
# To Research
- [x] is there a better way to manage dependencies other thatn `requirements.txt`. Is Pipfile better that requirements.txt. 
- [ ] chckout `pip-tools`


- [ ] better way to manage multipe virtual environments and multiple requirements files like `requirements-dev.txt` `requirements-live.txt`
- [ ] how to acheive public,private,protected in python inheritance
- [ ] what happens when you inherete from a class and what is `super().__init__()`
_______________________________________________
# Links to visit
- [ ] python's standard library documentation [here](https://docs.python.org/3.10/library/index.html#library-index)
- [ ] The Python Standard Library. The Python Language Reference gives a more formal definition of the language  [here](https://docs.python.org/3.10/reference/index.html#reference-index)
- [ ] Extending and Embedding the Python Interpreter and Python/C API Reference Manual [here](https://docs.python.org/3.10/extending/index.html#extending-index)
- [ ] copying in python [Here](https://docs.python.org/3/library/copy.html#shallow-vs-deep-copy)
# Tips
## To load .env
```py
from dotenv import find_dotenv, load_dotenv

load_dotenv(find_dotenv(), override=True)
```
- then to load a varialbe you simply write
```py
import os
variable=os.getnev('VARIABLE_NAME')
```
# Best pracices to structure your project
- Virtual Environments
- Package Management
- Modules and Packages
- Python Packaging
- \__init__.py Files
- Class-based Approach
- Configuration Files
- Logging
- Version Control
- Testing
- Documentation
- Linting and Code Formatting
- IDE and Editor Integration
_______________________________________________
# Best practices to document your code
- Docstrings
- Module-Level Comments
- README.md
- Project Structure and Architecture
- Function and Class Usage Examples
- API Documentation
- Changelog
- Type Annotations
- Use Jupyter Notebooks for Tutorials
- Version Control and Code Hosting Platform
_______________________________________________
# common errors i encounter
**error**
- you may encounter this error when you install requirements file
- `ERROR: Could not build wheels for backports.zoneinfo, which is required to install pyproject.toml-based projects`

**solution**
Edit your requirements.txt file

FROM:

`backports.zoneinfo==0.2.1`

TO:

`backports.zoneinfo;python_version<"3.9"`

---
# Interview questions
- [ ] what is the difference between concurrency and multiprocessing in python. how it works in python
- [ ] if i have a file on disk and i don't 2 threads to access or write on this file at the same time, how would you handle that. how would you implement this feature yourself withoug using any python features like context managers.
- [ ] how hashing works
- [ ] can the key of the dictionary in python be any data type other than strings
