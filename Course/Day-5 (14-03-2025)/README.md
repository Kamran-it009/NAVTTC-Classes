# Python Variable Naming Rules

1. **Start with a Letter or Underscore**: Variable names must start with a letter (a-z, A-Z) or an underscore (_). They cannot start with a digit (0-9).
   - Valid: `myVariable`, `_my_variable`
   - Invalid: `1variable`, `9name`

2. **Follow with Letters, Digits, or Underscores**: After the first character, variable names can contain letters, digits, or underscores.
   - Valid: `myVariable1`, `variable_2`
   - Invalid: `my-variable`, `my variable`

3. **Case Sensitivity**: Variable names are case-sensitive, meaning `myVariable` and `myvariable` are considered different variables.

4. **No Spaces**: Variable names cannot contain spaces. Use underscores to separate words.
   - Valid: `my_variable`
   - Invalid: `my variable`

5. **Reserved Words**: Avoid using Python reserved words or keywords as variable names (e.g., `class`, `for`, `if`, `else`, `True`, `False`, etc.). These words have special meanings in Python and cannot be used as variable names.
---
<br>

# Python Keywords

Introduction
Python keywords are reserved words that have special meaning in the Python programming language. These words define the syntax and structure of Python programs and cannot be used as variable names, function names, or any other identifiers.

## List of Python Keywords
Python provides a set of built-in keywords that serve various purposes in programming. The complete list of Python keywords can be obtained using the `keyword` module:

```python
import keyword
print(keyword.kwlist)
```

Here is a list of Python keywords as of Python 3.10:

```
False      await      else       import     pass
None       break      except     in         raise
True       class      finally    is         return
and        continue   for        lambda     try
as         def        from       nonlocal   while
assert     del        global     not        with
async      elif       if         or         yield
```

## Categories of Python Keywords
Python keywords can be grouped into different categories based on their usage.

### 1. Boolean Keywords
- `True` and `False`: Represent boolean values.
- `None`: Represents a null value or absence of value.

### 2. Control Flow Keywords
- `if`, `elif`, `else`: Used for conditional statements.
- `while`, `for`, `break`, `continue`, `pass`: Used in loop control.

### 3. Exception Handling Keywords
- `try`, `except`, `finally`, `raise`, `assert`: Used for handling exceptions and debugging.

### 4. Function and Class Keywords
- `def`: Defines a function.
- `return`: Returns a value from a function.
- `lambda`: Defines an anonymous function.
- `class`: Defines a class.

### 5. Variable Scope Keywords
- `global`: Declares a global variable.
- `nonlocal`: Declares a variable in an enclosing scope.

### 6. Logical Operators
- `and`, `or`, `not`: Used for logical operations.

### 7. Import Keywords
- `import`, `from`, `as`: Used for importing modules.

### 8. Context Management Keywords
- `with`: Used in resource management (e.g., file handling).

### 9. Asynchronous Programming Keywords
- `async`, `await`: Used in asynchronous programming.

## Conclusion
Understanding Python keywords is essential for writing efficient and error-free code. Since keywords are predefined and reserved, they should not be used for variable or function names. Learning these keywords helps in mastering Python programming.
