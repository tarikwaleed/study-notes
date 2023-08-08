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
___
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
___
# Topics to understand
- [ ] Context managers `__enter__` and `__exit__`
___
# Tips
- To load .env
```py
from dotenv import find_dotenv, load_dotenv

load_dotenv()
load_dotenv(find_dotenv(), override=True)
```
