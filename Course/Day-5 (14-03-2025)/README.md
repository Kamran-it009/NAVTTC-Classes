

# Python Variable Naming Rules

## 1. Rules for Naming Variables

In Python, variable names must follow certain rules:

- **Start with a Letter or Underscore**: Variable names must start with a letter (a-z, A-Z) or an underscore (_). They cannot start with a number (0-9).
  - ✅ Valid: `myVariable`, `_my_variable`
  - ❌ Invalid: `1variable`, `9name`

- **Can Include Letters, Numbers, or Underscores**: After the first character, variable names can contain letters, numbers, or underscores.
  - ✅ Valid: `myVariable1`, `variable_2`
  - ❌ Invalid: `my-variable`, `my variable`

- **Case-Sensitive**: Python treats variable names as case-sensitive, meaning `myVariable` and `myvariable` are different variables.

- **No Spaces**: Variable names cannot contain spaces. Use underscores (`_`) to separate words.
  - ✅ Valid: `my_variable`
  - ❌ Invalid: `my variable`

- **Cannot Use Reserved Words**: Avoid using Python keywords (like `class`, `for`, `if`, `else`, `True`, `False`) as variable names.

---

## 2. Python Keywords

### What Are Keywords?
Keywords are special words in Python that have predefined meanings. These words cannot be used as variable names or function names.

### List of Python Keywords
Python provides built-in keywords, which can be displayed using the `keyword` module:

```python
import keyword
print(keyword.kwlist)
```

Here are some common Python keywords:

```
False      await      else       import     pass
None       break      except     in         raise
True       class      finally    is         return
and        continue   for        lambda     try
as         def        from       nonlocal   while
assert     del        global     not        with
async      elif       if         or         yield
```

---

## 3. Formatted Strings in Python

### What Are Formatted Strings?
Formatted strings (f-strings) allow you to insert variables directly into strings in an easy way. They are created using the letter `f` before the string.

### Example Usage

```python
name = "Alice"
age = 25
print(f"My name is {name} and I am {age} years old.")
```
**Output:**
```
My name is Alice and I am 25 years old.
```

---

### ✅ Why Use f-Strings?
**f-Strings** (formatted string literals) are a modern way to embed expressions inside string literals using `{}` braces.

- **Easier to read and write** compared to older formatting methods  
- **Supports expressions** directly inside `{}`  
- **Faster performance** than `.format()` or `%` formatting  

---

#### 🔸 Example 1: Basic Variable Insertion
```python
name = "Ali"
age = 25
print(f"My name is {name} and I am {age} years old.")
```
**Output:**
```
My name is Ali and I am 25 years old.
```

---

#### 🔸 Example 2: Inline Expressions
```python
a = 5
b = 3
print(f"The sum of {a} and {b} is {a + b}.")
```
**Output:**
```
The sum of 5 and 3 is 8.
```

---

#### 🔸 Example 3: Formatting Output
```python
price = 49.99
print(f"The price is {price:.2f} dollars.")  # 2 decimal places
```
**Output:**
```
The price is 49.99 dollars.
```

---

## 4. 🔢 Arithmetic Operators

**Arithmetic operators** are used to perform basic mathematical operations such as addition, subtraction, multiplication, and so on.

| Operator | Description        | Example           |
|----------|--------------------|-------------------|
| `+`      | Adds two numbers   | `5 + 3 = 8`       |
| `-`      | Subtracts numbers  | `5 - 3 = 2`       |
| `*`      | Multiplies numbers | `5 * 3 = 15`      |
| `/`      | Divides and returns float | `5 / 3 = 1.67` |
| `//`     | Floor division (no decimal) | `5 // 3 = 1` |
| `%`      | Returns remainder  | `5 % 3 = 2`       |
| `**`     | Raises power       | `5 ** 3 = 125`    |

---

## 5. ⚖️ Comparison Operators

**Comparison operators** compare two values and return a Boolean result: either `True` or `False`.

| Operator | Description             | Example              |
|----------|-------------------------|----------------------|
| `==`     | Checks if equal         | `5 == 3 → False`     |
| `!=`     | Checks if not equal     | `5 != 3 → True`      |
| `>`      | Greater than            | `5 > 3 → True`       |
| `<`      | Less than               | `5 < 3 → False`      |
| `>=`     | Greater than or equal to| `5 >= 3 → True`      |
| `<=`     | Less than or equal to   | `5 <= 3 → False`     |

---

## 6. 🔗 Logical Operators

**Logical operators** allow you to combine multiple conditions. The result is also a Boolean (`True` or `False`).

| Operator | Description                                  | Example                       |
|----------|----------------------------------------------|-------------------------------|
| `and`    | Returns `True` if **both** conditions are true | `(5 > 3) and (3 > 1) → True`  |
| `or`     | Returns `True` if **at least one** condition is true | `(5 > 3) or (3 < 1) → True` |
| `not`    | Reverses the result of the condition          | `not(5 > 3) → False`          |

---

## 7. 🔤 Concatenation in Python

**String concatenation** is the process of joining two or more strings together using the `+` operator.

### Example
```python
str1 = "Hello"
str2 = "World"
result = str1 + " " + str2
print(result)
```
**Output:**
```
Hello World
```

---

## 8. 🧮 Assignment Operators

**Assignment operators** are used to assign values to variables and also perform operations at the same time.

| Operator | Description                | Example                        |
|----------|----------------------------|--------------------------------|
| `=`      | Assigns value              | `x = 5`                        |
| `+=`     | Adds and assigns           | `x += 3` → `x = x + 3`         |
| `-=`     | Subtracts and assigns      | `x -= 3` → `x = x - 3`         |
| `*=`     | Multiplies and assigns     | `x *= 3` → `x = x * 3`         |
| `/=`     | Divides and assigns        | `x /= 3` → `x = x / 3`         |
| `//=`    | Floor divides and assigns  | `x //= 3` → `x = x // 3`       |
| `%=`     | Modulus and assigns        | `x %= 3` → `x = x % 3`         |
| `**=`    | Exponentiates and assigns  | `x **= 3` → `x = x ** 3`       |

---
