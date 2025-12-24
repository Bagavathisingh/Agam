# Chapter 13: Keywords Reference (முக்கிய சொற்கள்)

## Complete Keyword List

agam supports both Tamil and English keywords. You can use either!

---

## Declaration Keywords

| Tamil | English | Description | Example |
|-------|---------|-------------|---------|
| `செயல்` | `fn` | Define a function | `செயல் greet():` |
| `மாறி` | `let` | Declare a variable | `மாறி x = 10` |
| `மாறாத` | `const` | Declare a constant | `மாறாத PI = 3.14` |

---

## Control Flow Keywords

| Tamil | English | Description | Example |
|-------|---------|-------------|---------|
| `என்றால்` | `if` | If condition | `என்றால் x > 5:` |
| `இல்லையென்றால்` | `elif` | Else if | `இல்லையென்றால் x > 3:` |
| `இல்லை` | `else` | Else | `இல்லை:` |
| `வரை` | `while` | While loop | `வரை x < 10:` |
| `ஒவ்வொரு` | `for` | For loop | `ஒவ்வொரு i உள்ள items:` |
| `உள்ள` | `in` | In operator | `x உள்ள list` |
| `திரும்பு` | `return` | Return value | `திரும்பு result` |
| `நிறுத்து` | `break` | Break loop | `நிறுத்து` |
| `தொடர்` | `continue` | Continue loop | `தொடர்` |

---

## Boolean Keywords

| Tamil | English | Description | Example |
|-------|---------|-------------|---------|
| `உண்மை` | `true` | Boolean true | `மாறி flag = உண்மை` |
| `பொய்` | `false` | Boolean false | `மாறி flag = பொய்` |
| `இல்லா` | `null` | Null value | `மாறி data = இல்லா` |

---

## Logical Operators

| Tamil | English | Description | Example |
|-------|---------|-------------|---------|
| `மற்றும்` | `and` | Logical AND | `x > 0 மற்றும் x < 10` |
| `அல்லது` | `or` | Logical OR | `x < 0 அல்லது x > 10` |
| `இல்ல` | `not` | Logical NOT | `இல்ல is_empty` |

---

## Module Keywords

| Tamil | English | Description | Example |
|-------|---------|-------------|---------|
| `இறக்குமதி` | `import` | Import a module | `இறக்குமதி math_utils` |
| `இருந்து` | `from` | From (for selective imports) | `இருந்து math_utils இறக்குமதி add` |

### Import Examples

```
# Import entire module
இறக்குமதி math_utils

# Import specific items from module
இருந்து math_utils இறக்குமதி add, subtract
```

---

## Error Handling Keywords

| Tamil | English | Description | Example |
|-------|---------|-------------|---------|
| `முயற்சி` | `try` | Try block | `முயற்சி:` |
| `பிடி` | `catch` | Catch block | `பிடி error:` |
| `வீசு` | `throw` | Throw an error | `வீசு("Error message")` |

### Error Handling Example

```
முயற்சி:
    மாறி result = risky_operation()
    அச்சிடு(result)
பிடி error:
    அச்சிடு("Error occurred:", error)
```

---

## Struct Keywords

| Tamil | English | Description | Example |
|-------|---------|-------------|---------|
| `கட்டமைப்பு` | `struct` | Define a structure | `கட்டமைப்பு Person:` |

### Struct Example

```
கட்டமைப்பு Person:
    name
    age

மாறி person = Person("Raja", 25)
அச்சிடு(person.name)   # Output: Raja
```

---

## Enum Keywords

| Tamil | English | Description | Example |
|-------|---------|-------------|---------|
| `விருப்பம்` | `enum` | Define an enumeration | `விருப்பம் Color:` |

### Enum Example

```
விருப்பம் Color:
    Red
    Green
    Blue

மாறி color = Color.Red
```

---

## Pattern Matching Keywords

| Tamil | English | Description | Example |
|-------|---------|-------------|---------|
| `பொருத்து` | `match` | Match expression | `பொருத்து value:` |
| `_` | `_` | Wildcard pattern | `_ => default_case` |
| `=>` | `=>` | Match arm arrow | `1 => handle_one()` |

### Pattern Matching Example

```
மாறி grade = 85

பொருத்து grade:
    90 => அச்சிடு("A+")
    80 => அச்சிடு("A")
    70 => அச்சிடு("B")
    _ => அச்சிடு("Below B")
```

---

## Built-in Functions

### I/O Functions

| Tamil | English | Description |
|-------|---------|-------------|
| `அச்சிடு` | `print` | Print output |
| `உள்ளீடு` | `input` | Read input |

### Type Functions

| Tamil | English | Description |
|-------|---------|-------------|
| `நீளம்` | `len` | Get length |
| `வகை` | `type` | Get type |
| `எண்ணாக` | `int` | Convert to integer |
| `தசமாக` | `float` | Convert to float |
| `சரமாக` | `str` | Convert to string |

### Collection Functions

| Tamil | English | Description |
|-------|---------|-------------|
| `வரம்பு` | `range` | Create range |
| `சேர்` | `append` | Add to list |
| `நீக்கு` | `pop` | Remove from list |
| `வரிசை` | `sort` | Sort list |
| `தலைகீழ்` | `reverse` | Reverse list/string |

### Math Functions

| Tamil | English | Description |
|-------|---------|-------------|
| `வர்க்கம்` | `sqrt` | Square root |
| `அடி` | `pow` | Power |
| `தளம்` | `floor` | Round down |
| `கூரை` | `ceil` | Round up |
| `முழுமை` | `abs` | Absolute value |
| `குறைந்தபட்சம்` | `min` | Minimum value |
| `அதிகபட்சம்` | `max` | Maximum value |
| `கூட்டு` | `sum` | Sum of list |
| `தற்செயல்` | `random` | Random number |

### String Functions

| Tamil | English | Description |
|-------|---------|-------------|
| `பிரி` | `split` | Split string |
| `இணை` | `join` | Join list to string |
| `மேல்` | `upper` | Uppercase |
| `கீழ்` | `lower` | Lowercase |
| `ஒழுங்கு` | `trim` | Trim whitespace |
| `மாற்று` | `replace` | Replace text |
| `தொடங்கு` | `startswith` | Check prefix |
| `முடிவு` | `endswith` | Check suffix |
| `உள்ளதா` | `contains` | Check contains |

### File I/O Functions

| Tamil | English | Description |
|-------|---------|-------------|
| `படி` | `read_file` | Read file contents |
| `எழுது` | `write_file` | Write to file |
| `உள்ளது` | `file_exists` | Check if file exists |

### System Functions

| Tamil | English | Description |
|-------|---------|-------------|
| `வெளியேறு` | `exit` | Exit program |

---

## Operators

### Arithmetic

| Operator | Description | Example |
|----------|-------------|---------|
| `+` | Addition | `5 + 3` → `8` |
| `-` | Subtraction | `5 - 3` → `2` |
| `*` | Multiplication | `5 * 3` → `15` |
| `/` | Division | `5 / 2` → `2.5` |
| `%` | Modulo | `5 % 2` → `1` |

### Comparison

| Operator | Description | Example |
|----------|-------------|---------|
| `==` | Equal | `5 == 5` → `உண்மை` |
| `!=` | Not equal | `5 != 3` → `உண்மை` |
| `<` | Less than | `3 < 5` → `உண்மை` |
| `>` | Greater than | `5 > 3` → `உண்மை` |
| `<=` | Less or equal | `3 <= 3` → `உண்மை` |
| `>=` | Greater or equal | `5 >= 5` → `உண்மை` |

---

## Quick Reference Card

```
# Variable
மாறி name = value

# Constant
மாறாத NAME = value

# Function
செயல் name(params):
    code
    திரும்பு value

# If/Else
என்றால் condition:
    code
இல்லையென்றால் condition:
    code
இல்லை:
    code

# While Loop
வரை condition:
    code

# For Loop
ஒவ்வொரு item உள்ள collection:
    code

# Struct
கட்டமைப்பு Name:
    field1
    field2

# Enum
விருப்பம் Name:
    Variant1
    Variant2

# Pattern Matching
பொருத்து value:
    pattern1 => result1
    pattern2 => result2
    _ => default

# Try-Catch
முயற்சி:
    risky_code
பிடி error:
    handle_error

# Import
இறக்குமதி module_name
இருந்து module_name இறக்குமதி item1, item2

# Print
அச்சிடு(value)

# Input
மாறி x = உள்ளீடு("prompt")
```

---

## Complete Keywords Summary

| Category | Tamil Keywords |
|----------|---------------|
| **Declarations** | `செயல்`, `மாறி`, `மாறாத` |
| **Control Flow** | `என்றால்`, `இல்லையென்றால்`, `இல்லை`, `வரை`, `ஒவ்வொரு`, `உள்ள`, `திரும்பு`, `நிறுத்து`, `தொடர்` |
| **Booleans** | `உண்மை`, `பொய்`, `இல்லா` |
| **Logical** | `மற்றும்`, `அல்லது`, `இல்ல` |
| **Modules** | `இறக்குமதி`, `இருந்து` |
| **Error Handling** | `முயற்சி`, `பிடி`, `வீசு` |
| **Data Structures** | `கட்டமைப்பு`, `விருப்பம்` |
| **Pattern Matching** | `பொருத்து` |

---

**Next: [Chapter 14: Error Messages →](14_errors.md)**
