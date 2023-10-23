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

- [ ] Context managers `__enter__` and `__exit__`
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
_______________________________________________
# To Research
- [ ] is there a better way to manage dependencies other thatn `requirements.txt`. Is Pipfile better that requirements.txt
- [ ] better way to manage multipe virtual environments and multiple requirements files like `requirements-dev.txt` `requirements-live.txt`
_______________________________________________
# Tips
- To load .env
```py
from dotenv import find_dotenv, load_dotenv

load_dotenv()
load_dotenv(find_dotenv(), override=True)
```
