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
<h1 style="color:navy">Topics to understand</h1>

- [x] Context managers `__enter__` and `__exit__`
- [ ] <span style="color: navy;">decorators</span>
- [ ] classmethod
- [ ] static method
- [ ] @property
- [ ] @namesetter
- [ ] yield
- [ ] generators
- [ ] map,filter,reduce,enumerate,zip,counter, ...
- [ ] lambda function
- [ ] advanced list comperhension
- [ ] iterators
- [ ] why there is no overloading in python
- [ ] dunder methods, know them all
- [ ] metaclasses
- [ ] descriptors
- [ ] dependency intection and inversion of control
- [ ] ABC module, `@abstractmethod`
- [ ] async python
- [ ] namespaces and scope in python [Here](https://realpython.com/python-namespaces-scope/)
- [ ] mutabilty and immutability in python
- [x] `args` and `**kwargs`
- [ ] how this syntax is possble
```python
    "DIRS": [BASE_DIR / "templates"],
```


_______________________________________________
# To Research
- [ ] is there a better way to manage dependencies other thatn `requirements.txt`. Is Pipfile better that requirements.txt. 
- [ ] chckout `pip-tools`

- [ ] better way to manage multipe virtual environments and multiple requirements files like `requirements-dev.txt` `requirements-live.txt`
_______________________________________________
# Links to visit
- [ ] python's standard library documentation [here](https://docs.python.org/3.10/library/index.html#library-index)
- [ ] The Python Standard Library. The Python Language Reference gives a more formal definition of the language  [here](https://docs.python.org/3.10/reference/index.html#reference-index)
- [ ] Extending and Embedding the Python Interpreter and Python/C API Reference Manual [here](https://docs.python.org/3.10/extending/index.html#extending-index)
- [ ] copying in python [Here](https://docs.python.org/3/library/copy.html#shallow-vs-deep-copy)
# Tips
- To load .env
```py
from dotenv import find_dotenv, load_dotenv

load_dotenv()
load_dotenv(find_dotenv(), override=True)
```
