# Chapter 15: Structs (கட்டமைப்பு)

## Overview

Structs allow you to create custom data types by grouping related values together. In agam, you use `கட்டமைப்பு` (struct) to define a structure.

---

## Defining a Struct

Use `கட்டமைப்பு` followed by the struct name and its fields:

```
கட்டமைப்பு Person:
    name
    age
    city
```

---

## Creating Struct Instances

Create an instance by calling the struct like a function:

```
கட்டமைப்பு Person:
    name
    age
    city

# Create a person
மாறி person1 = Person("ராஜா", 25, "சென்னை")
மாறி person2 = Person("கமலா", 30, "மதுரை")
```

---

## Accessing Fields

Use the dot (`.`) operator to access struct fields:

```
கட்டமைப்பு Person:
    name
    age
    city

மாறி person = Person("ராஜா", 25, "சென்னை")

# Access fields
அச்சிடு(person.name)    # Output: ராஜா
அச்சிடு(person.age)     # Output: 25
அச்சிடு(person.city)    # Output: சென்னை
```

---

## Modifying Fields

You can modify struct fields after creation:

```
கட்டமைப்பு Person:
    name
    age

மாறி person = Person("ராஜா", 25)
அச்சிடு(person.age)     # Output: 25

# Modify field
person.age = 26
அச்சிடு(person.age)     # Output: 26
```

---

## Structs with Functions

Create functions that work with your structs:

```
கட்டமைப்பு Rectangle:
    width
    height

செயல் area(rect):
    திரும்பு rect.width * rect.height

செயல் perimeter(rect):
    திரும்பு 2 * (rect.width + rect.height)

மாறி box = Rectangle(10, 5)
அச்சிடு("Area:", area(box))           # Output: Area: 50
அச்சிடு("Perimeter:", perimeter(box)) # Output: Perimeter: 30
```

---

## Practical Examples

### Example 1: Student Records

```
கட்டமைப்பு Student:
    name
    roll_number
    marks

செயல் get_grade(student):
    என்றால் student.marks >= 90:
        திரும்பு "A+"
    இல்லையென்றால் student.marks >= 80:
        திரும்பு "A"
    இல்லையென்றால் student.marks >= 70:
        திரும்பு "B"
    இல்லையென்றால் student.marks >= 60:
        திரும்பு "C"
    இல்லை:
        திரும்பு "F"

மாறி student1 = Student("அருண்", 101, 85)
மாறி student2 = Student("பிரியா", 102, 92)

அச்சிடு(student1.name, "Grade:", get_grade(student1))
அச்சிடு(student2.name, "Grade:", get_grade(student2))
```

### Example 2: Point and Distance

```
கட்டமைப்பு Point:
    x
    y

செயல் distance(p1, p2):
    மாறி dx = p2.x - p1.x
    மாறி dy = p2.y - p1.y
    திரும்பு வர்க்கம்(dx * dx + dy * dy)

மாறி point1 = Point(0, 0)
மாறி point2 = Point(3, 4)

அச்சிடு("Distance:", distance(point1, point2))  # Output: Distance: 5
```

### Example 3: Bank Account

```
கட்டமைப்பு Account:
    holder
    balance

செயல் deposit(account, amount):
    account.balance = account.balance + amount
    அச்சிடு("Deposited:", amount)
    அச்சிடு("New balance:", account.balance)

செயல் withdraw(account, amount):
    என்றால் amount > account.balance:
        அச்சிடு("Insufficient balance!")
    இல்லை:
        account.balance = account.balance - amount
        அச்சிடு("Withdrawn:", amount)
        அச்சிடு("Remaining:", account.balance)

மாறி my_account = Account("ராஜா", 1000)
deposit(my_account, 500)
withdraw(my_account, 200)
```

---

## Nested Structs

You can use structs inside other structs:

```
கட்டமைப்பு Address:
    street
    city
    pincode

கட்டமைப்பு Employee:
    name
    id
    address

மாறி addr = Address("123 Main St", "Chennai", "600001")
மாறி emp = Employee("Kumar", 1001, addr)

அச்சிடு(emp.name)              # Output: Kumar
அச்சிடு(emp.address.city)      # Output: Chennai
அச்சிடு(emp.address.pincode)   # Output: 600001
```

---

## List of Structs

Store multiple struct instances in a list:

```
கட்டமைப்பு Product:
    name
    price

மாறி products = [
    Product("Apple", 50),
    Product("Banana", 30),
    Product("Orange", 40)
]

செயல் total_cost(items):
    மாறி total = 0
    ஒவ்வொரு item உள்ள items:
        total = total + item.price
    திரும்பு total

அச்சிடு("Total:", total_cost(products))  # Output: Total: 120
```

---

## Summary

- Use `கட்டமைப்பு` to define custom data types
- Create instances by calling the struct name with arguments
- Access and modify fields using the dot (`.`) operator
- Combine with functions for powerful data modeling
- Nest structs for complex data structures

---

**Next: [Chapter 16: Enums →](16_enums.md)**
