# Chapter 16: Enums (விருப்பம்)

## Overview

Enums (enumerations) allow you to define a type with a fixed set of possible values. In agam, you use `விருப்பம்` (enum) to define an enumeration.

---

## Defining an Enum

Use `விருப்பம்` followed by the enum name and its variants:

```
விருப்பம் Color:
    Red
    Green
    Blue
```

---

## Using Enum Values

Access enum variants using the dot (`.`) operator:

```
விருப்பம் Color:
    Red
    Green
    Blue

மாறி favorite = Color.Red
மாறி secondary = Color.Blue

அச்சிடு(favorite)    # Output: Color.Red
```

---

## Comparing Enum Values

Compare enum values using `==`:

```
விருப்பம் Status:
    Active
    Inactive
    Pending

மாறி status = Status.Active

என்றால் status == Status.Active:
    அச்சிடு("System is active!")
இல்லையென்றால் status == Status.Pending:
    அச்சிடு("System is pending...")
இல்லை:
    அச்சிடு("System is inactive.")
```

---

## Practical Examples

### Example 1: Days of the Week

```
விருப்பம் Day:
    Monday
    Tuesday
    Wednesday
    Thursday
    Friday
    Saturday
    Sunday

செயல் is_weekend(day):
    என்றால் day == Day.Saturday அல்லது day == Day.Sunday:
        திரும்பு உண்மை
    திரும்பு பொய்

மாறி today = Day.Saturday
என்றால் is_weekend(today):
    அச்சிடு("It's the weekend! 🎉")
இல்லை:
    அச்சிடு("It's a workday.")
```

### Example 2: Traffic Light

```
விருப்பம் TrafficLight:
    Red
    Yellow
    Green

செயல் action(light):
    என்றால் light == TrafficLight.Red:
        திரும்பு "Stop!"
    இல்லையென்றால் light == TrafficLight.Yellow:
        திரும்பு "Slow down..."
    இல்லை:
        திரும்பு "Go!"

மாறி current = TrafficLight.Green
அச்சிடு(action(current))  # Output: Go!
```

### Example 3: Order Status

```
விருப்பம் OrderStatus:
    Placed
    Processing
    Shipped
    Delivered
    Cancelled

கட்டமைப்பு Order:
    id
    product
    status

செயல் update_status(order, new_status):
    order.status = new_status
    அச்சிடு("Order", order.id, "is now:", new_status)

மாறி order = Order(1001, "Laptop", OrderStatus.Placed)
update_status(order, OrderStatus.Processing)
update_status(order, OrderStatus.Shipped)
update_status(order, OrderStatus.Delivered)
```

### Example 4: Direction

```
விருப்பம் Direction:
    North
    South
    East
    West

கட்டமைப்பு Position:
    x
    y

செயல் move(pos, direction):
    என்றால் direction == Direction.North:
        pos.y = pos.y + 1
    இல்லையென்றால் direction == Direction.South:
        pos.y = pos.y - 1
    இல்லையென்றால் direction == Direction.East:
        pos.x = pos.x + 1
    இல்லை:
        pos.x = pos.x - 1

மாறி player = Position(0, 0)
move(player, Direction.North)
move(player, Direction.East)
அச்சிடு("Position:", player.x, player.y)  # Output: Position: 1 1
```

---

## Enums with Pattern Matching

Use `பொருத்து` (match) for cleaner enum handling:

```
விருப்பம் Season:
    Spring
    Summer
    Autumn
    Winter

செயல் describe(season):
    பொருத்து season:
        Season.Spring => திரும்பு "Flowers bloom 🌸"
        Season.Summer => திரும்பு "Hot and sunny ☀️"
        Season.Autumn => திரும்பு "Leaves fall 🍂"
        Season.Winter => திரும்பு "Cold and snowy ❄️"

மாறி current = Season.Winter
அச்சிடு(describe(current))  # Output: Cold and snowy ❄️
```

---

## When to Use Enums

Enums are useful when you have:

- A **fixed set of options** (colors, days, statuses)
- **State machines** (order status, game states)
- **Configuration options** (log levels, modes)
- **Type-safe alternatives** to string constants

---

## Summary

- Use `விருப்பம்` to define enumerations
- Access variants with dot notation: `EnumName.Variant`
- Compare using `==`
- Combine with `பொருத்து` for clean pattern matching
- Great for representing fixed sets of values

---

**Next: [Chapter 17: Pattern Matching →](17_pattern_matching.md)**
