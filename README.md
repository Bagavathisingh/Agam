<p align="center">
  <img src="assets/agam-banner.svg" alt="Agam Tamil Programming Language" />
</p>

<p align="center">
  <img src="https://img.shields.io/github/v/release/Aruvili/Agam" />
  <img src="https://img.shields.io/badge/docs-agam.aruvili.com-brightgreen" />
  <img src="https://img.shields.io/github/license/Aruvili/Agam" />
  <img src="https://img.shields.io/github/stars/Aruvili/Agam?style=social" />
</p>

---

# 🔥 அகம் (Agam) — Tamil Programming Language

> **Program in Tamil. Build for the real world.**

**அகம் (Agam)** is a **modern, fast, and safe Tamil-first programming language** designed for learning, scripting, and future production use.  
It combines **Python-like simplicity** with **Rust-powered performance and safety**.

---

## ✨ Why Agam?

- 🇮🇳 Write programs **entirely in Tamil**
- 🐍 Simple, readable, Python-inspired syntax
- ⚡ High performance (built with Rust)
- 🔒 Memory-safe and type-secure
- 🖥️ Interactive REPL
- 🎓 Perfect for education & beginners
- 🚀 Built with long-term production goals

---

## 🚀 Quick Example

```agam
அச்சிடு("வணக்கம் உலகம்!")
````

**Output**

```
வணக்கம் உலகம்!
```

---

## 🧩 Language Basics

### Variables & Constants

```agam
மாறி பெயர் = "தமிழ்"
மாறி வயது = 25
மாறாத பை = 3.14159

அச்சிடு(பெயர்)
```

---

### Conditionals

```agam
மாறி மதிப்பெண் = 85

என்றால் மதிப்பெண் >= 90:
    அச்சிடு("தர நிலை: அ+")
இல்லையென்றால் மதிப்பெண் >= 80:
    அச்சிடு("தர நிலை: அ")
இல்லை:
    அச்சிடு("மேம்படுத்த வேண்டும்")
```

---

### Loops

```agam
# While loop
மாறி எண் = 1
வரை எண் <= 5:
    அச்சிடு(எண்)
    எண் = எண் + 1
```

```agam
# For loop
ஒவ்வொரு எண் உள்ள வரம்பு(1, 6):
    அச்சிடு(எண்)
```

---

### Functions

```agam
செயல் வணக்கம்(பெயர்):
    திரும்பு "வணக்கம், " + பெயர் + "!"

அச்சிடு(வணக்கம்("நண்பா"))
```

**Output**

```
வணக்கம், நண்பா!
```

---

## 📖 Supported Keywords

### Core Keywords

| Tamil           | English  | Purpose       |
| --------------- | -------- | ------------- |
| `செயல்`         | `fn`     | Function      |
| `மாறி`          | `let`    | Variable      |
| `மாறாத`         | `const`  | Constant      |
| `என்றால்`       | `if`     | Conditional   |
| `இல்லையென்றால்` | `elif`   | Else-if       |
| `இல்லை`         | `else`   | Else          |
| `வரை`           | `while`  | While loop    |
| `ஒவ்வொரு`       | `for`    | For loop      |
| `உள்ள`          | `in`     | In            |
| `திரும்பு`      | `return` | Return        |
| `நிறுத்து`      | `break`  | Break loop    |
| `தொடர்`         | `continue` | Continue loop |
| `உண்மை`         | `true`   | Boolean true  |
| `பொய்`          | `false`  | Boolean false |
| `இல்லா`         | `null`   | Null value    |
| `மற்றும்`       | `and`    | Logical AND   |
| `அல்லது`        | `or`     | Logical OR    |
| `இல்ல`          | `not`    | Logical NOT   |

### Advanced Features

| Tamil           | English  | Purpose           |
| --------------- | -------- | ----------------- |
| `கட்டமைப்பு`    | `struct` | Define struct     |
| `விருப்பம்`     | `enum`   | Define enum       |
| `பொருத்து`      | `match`  | Pattern matching  |
| `இறக்குமதி`     | `import` | Import module     |
| `இருந்து`       | `from`   | From (for imports)|
| `முயற்சி`       | `try`    | Try block         |
| `பிடி`          | `catch`  | Catch block       |
| `வீசு`          | `throw`  | Throw error       |

### Built-in Functions

| Tamil          | English     | Purpose           |
| -------------- | ----------- | ----------------- |
| `அச்சிடு`      | `print`     | Output            |
| `உள்ளீடு`      | `input`     | Input             |
| `நீளம்`        | `len`       | Get length        |
| `வகை`          | `type`      | Get type          |
| `வரம்பு`       | `range`     | Number range      |
| `வர்க்கம்`     | `sqrt`      | Square root       |
| `படி`          | `read_file` | Read file         |
| `எழுது`        | `write_file`| Write file        |

> 📚 See the [complete documentation](docs/README.md) for all 33+ built-in functions!

---

## 🖥️ Interactive REPL

Launch the REPL:

```bash
agam
```

No setup. No dependencies. Just run.

---

## 📘 Documentation

Complete and official documentation is available at:

🌐 **[https://agam.aruvili.com](https://agam.aruvili.com)**

Includes:

* Getting started
* Language syntax & keywords
* Conditions, loops, functions
* Lambda expressions
* Standard library
* REPL usage
* Examples & FAQs

---

## 👨‍💻 Credits

### 🧠 Language

* **Created by:** [**Balapriyan B**](https://github.com/BalaPriyan)
* **Assisted by:** Claude Sonnet 4.5

### 🖥️ Tested
* **Language Tested By**: [**Sriram G**](https://github.com/GGSriram)

### 📘 Documentation

* **Developed by:** [**Bagavathisingh B**](https://github.com/Bagavathisingh)
* **Hosted at:** [https://agam.aruvili.com](https://agam.aruvili.com)

### 📝 README 
* **crafted by**: **ChatGPT**

---

## 🤝 Contributing

Agam is **open-source and community-driven** ❤️
Contributions, ideas, issues, and improvements are always welcome.

⭐ If you like Agam, please **star the repository** — it helps the Tamil developer ecosystem grow.

---

## 📜 License

MIT License © Aruvili

---

### 🇮🇳 **அகம் — தமிழில் நிரலாக்கத்தின் எதிர்காலம்**

Built with ❤️ for the Tamil developer community

---
