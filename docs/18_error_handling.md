# Chapter 18: Error Handling (பிழை கையாளுதல்)

## Overview

Error handling allows your program to gracefully handle unexpected situations. In agam, you use `முயற்சி` (try), `பிடி` (catch), and `வீசு` (throw) for error handling.

---

## Basic Syntax

```
முயற்சி:
    # Code that might fail
    risky_operation()
பிடி error:
    # Handle the error
    அச்சிடு("Error:", error)
```

---

## Try-Catch Example

```
முயற்சி:
    மாறி result = 10 / 0
    அச்சிடு(result)
பிடி error:
    அச்சிடு("An error occurred!")
    அச்சிடு("Details:", error)
```

---

## Throwing Errors

Use `வீசு` (throw) to raise an error:

```
செயல் check_age(age):
    என்றால் age < 0:
        வீசு("Age cannot be negative!")
    என்றால் age > 150:
        வீசு("Age is too high!")
    திரும்பு "Valid age"

முயற்சி:
    மாறி result = check_age(-5)
    அச்சிடு(result)
பிடி error:
    அச்சிடு("Error:", error)
```

---

## Error Messages in Tamil

agam provides error messages in Tamil for better understanding:

```
முயற்சி:
    மாறி x = எண்ணாக("hello")  # Invalid conversion
பிடி error:
    அச்சிடு(error)
# Output: 'hello' எண்ணாக மாற்ற இயலவில்லை
```

---

## Practical Examples

### Example 1: Safe Division

```
செயல் safe_divide(a, b):
    என்றால் b == 0:
        வீசு("Cannot divide by zero!")
    திரும்பு a / b

முயற்சி:
    அச்சிடு(safe_divide(10, 2))   # Output: 5
    அச்சிடு(safe_divide(10, 0))   # This will throw
பிடி error:
    அச்சிடு("Division error:", error)
```

### Example 2: File Reading

```
செயல் read_config(filename):
    என்றால் இல்ல உள்ளது(filename):
        வீசு("Config file not found: " + filename)
    திரும்பு படி(filename)

முயற்சி:
    மாறி config = read_config("settings.txt")
    அச்சிடு("Config loaded:", config)
பிடி error:
    அச்சிடு("Failed to load config")
    அச்சிடு("Error:", error)
    # Use default settings
    மாறி config = "default settings"
```

### Example 3: Input Validation

```
செயல் get_positive_number():
    மாறி input_str = உள்ளீடு("Enter a positive number: ")
    
    முயற்சி:
        மாறி num = எண்ணாக(input_str)
        என்றால் num <= 0:
            வீசு("Number must be positive!")
        திரும்பு num
    பிடி error:
        அச்சிடு("Invalid input:", error)
        திரும்பு get_positive_number()  # Retry

மாறி number = get_positive_number()
அச்சிடு("You entered:", number)
```

### Example 4: Bank Transaction

```
கட்டமைப்பு Account:
    name
    balance

செயல் withdraw(account, amount):
    என்றால் amount <= 0:
        வீசு("Withdrawal amount must be positive!")
    என்றால் amount > account.balance:
        வீசு("Insufficient funds! Available: " + சரமாக(account.balance))
    
    account.balance = account.balance - amount
    திரும்பு account.balance

மாறி my_account = Account("Raja", 1000)

முயற்சி:
    withdraw(my_account, 500)
    அச்சிடு("Withdrawal successful!")
    அச்சிடு("New balance:", my_account.balance)
    
    withdraw(my_account, 600)  # This will fail
பிடி error:
    அச்சிடு("Transaction failed:", error)
```

### Example 5: Array Index Safety

```
செயல் safe_get(list, index):
    என்றால் index < 0 அல்லது index >= நீளம்(list):
        வீசு("Index out of bounds: " + சரமாக(index))
    திரும்பு list[index]

மாறி items = ["apple", "banana", "cherry"]

முயற்சி:
    அச்சிடு(safe_get(items, 1))   # Output: banana
    அச்சிடு(safe_get(items, 10))  # This will throw
பிடி error:
    அச்சிடு("Access error:", error)
```

---

## Error Handling Patterns

### Pattern 1: Default Value on Error

```
செயல் parse_number(text, default):
    முயற்சி:
        திரும்பு எண்ணாக(text)
    பிடி error:
        திரும்பு default

மாறி value = parse_number("abc", 0)
அச்சிடு(value)  # Output: 0
```

### Pattern 2: Retry Logic

```
செயல் retry_operation(max_attempts):
    மாறி attempts = 0
    
    வரை attempts < max_attempts:
        முயற்சி:
            # Simulate operation that might fail
            என்றால் தற்செயல்() < 0.7:
                வீசு("Random failure!")
            அச்சிடு("Success!")
            திரும்பு உண்மை
        பிடி error:
            attempts = attempts + 1
            அச்சிடு("Attempt", attempts, "failed:", error)
    
    அச்சிடு("All attempts failed!")
    திரும்பு பொய்

retry_operation(3)
```

### Pattern 3: Cleanup on Error

```
செயல் process_file(filename):
    மாறி file_opened = பொய்
    
    முயற்சி:
        என்றால் உள்ளது(filename):
            மாறி content = படி(filename)
            file_opened = உண்மை
            
            # Process content
            மாறி processed = மேல்(content)
            எழுது("output.txt", processed)
            
            அச்சிடு("File processed successfully!")
        இல்லை:
            வீசு("File not found!")
    பிடி error:
        அச்சிடு("Processing failed:", error)
        
        # Cleanup
        என்றால் file_opened:
            அச்சிடு("Cleaning up...")
```

### Pattern 4: Error Propagation

```
செயல் low_level_operation():
    வீசு("Low level error!")

செயல் mid_level_operation():
    முயற்சி:
        low_level_operation()
    பிடி error:
        வீசு("Mid level failed: " + error)

செயல் high_level_operation():
    முயற்சி:
        mid_level_operation()
    பிடி error:
        அச்சிடு("High level caught:", error)

high_level_operation()
```

---

## Common Error Scenarios

| Scenario | How to Handle |
|----------|---------------|
| Division by zero | Check before dividing or use try-catch |
| Invalid input | Validate input and throw descriptive errors |
| File not found | Check with `உள்ளது()` before reading |
| Out of bounds | Check index against length |
| Type conversion | Use try-catch around conversion functions |

---

## Best Practices

1. **Be specific with error messages** - Include helpful details
2. **Handle errors at the appropriate level** - Don't catch too early
3. **Use validation before operations** - Prevent errors when possible
4. **Provide fallback behavior** - Default values or retry logic
5. **Log errors for debugging** - Print error details

---

## Summary

- Use `முயற்சி` (try) to wrap code that might fail
- Use `பிடி` (catch) to handle errors
- Use `வீசு` (throw) to raise custom errors
- Provide clear, descriptive error messages
- Always have a recovery strategy

---

**Next: [Chapter 19: Modules →](19_modules.md)**
