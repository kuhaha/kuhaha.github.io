# Coding Rules
## Directories/Files
1. name local/private variables/functions/modules with a leading undersoce, such as `_mymodule.py`
2. alias imported modules with a leading undersocre, such as
```
  import scipy as _sp
  import numpy as _np
  import pandas as _pd
```
3. package related modules in a directory
4. create an `__init__.py` file in package directory, export the most common interface
    - `__all__` is a list of public objects of that module, as interpreted by `import *`, such as `__all__= ["foo", "bar"]`. It overrides the default of hiding everything that begins with an underscore. 
6. [optionally] put packages/subpackages under namespace 

## Code Layout - pep8
1. Use 4 spaces per indentation level.
2. Limit all lines to a maximum of 79 characters.
3. Surround top-level function and class definitions with two blank lines.
4. Method definitions inside a class are surrounded by a single blank line.
5. Imports should usually be on separate lines
6. Imports are always put at the top of the file, just after any module comments and docstrings,
  and before module globals and constants.
7. Absolute imports are recommended. However, explicit relative imports are an acceptable
  alternative to absolute imports, especially when dealing with complex package layouts
  where using absolute imports would be unnecessarily verbose
8. Wildcard imports (from <module> import *) should be avoided.
9. Module level “dunders” (i.e. names with two leading and two trailing underscores) such as
  `__all__`, `__author__`, `__version__`, etc. should be placed after the module docstring 
  but before any import statements except from __future__ imports. 
