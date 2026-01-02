# λ Algolang

<div align="center">

![Algolang Logo](https://img.shields.io/badge/λ-Algolang-00d9ff?style=for-the-badge&labelColor=0a0e14)
![Version](https://img.shields.io/badge/version-3.5-a371f7?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-3fb950?style=for-the-badge)
![No Dependencies](https://img.shields.io/badge/dependencies-none-ff79c6?style=for-the-badge)

**A beginner-friendly programming language for learning algorithms, boolean logic, and building interactive apps.**

[Live Demo](#demo) • [Features](#features) • [Quick Start](#quick-start) • [Documentation](#documentation) • [Examples](#examples)

</div>

---

## ✨ Features

- 🎓 **Beginner Friendly** - Simple syntax designed for learning
- 🧮 **Algorithm Functions** - Built-in fibonacci, factorial, primes, GCD, and more
- 🔘 **Boolean Logic** - AND, OR, NOT, XOR, NAND, NOR with truth table generation
- 🎨 **UI Components** - Buttons, badges, cards, progress bars, tables
- 🎮 **Interactive Apps** - Build clicker games, calculators, quizzes
- 📦 **Module System** - Import only what you need (`%import console`)
- 📊 **Statistics** - Mean, median, standard deviation, array operations
- 🌐 **Zero Dependencies** - Single HTML file, runs entirely in browser
- 📱 **Mobile Friendly** - Responsive design with touch support

## 🚀 Quick Start

### Option 1: Use Online
Simply open `algolang.html` in any modern browser.

### Option 2: Clone Repository
```bash
git clone https://github.com/yourusername/algolang.git
cd algolang
open algolang.html
```

### Your First Program
```
%import console

print("Hello, Algolang!")
print("2 + 2 = " + (2 + 2))
```

## 📦 Module System

Algolang uses a modular import system. Import modules at the top of your code:

| Module | Features | Use Case |
|--------|----------|----------|
| `%import console` | `print()` | Text output |
| `%import app` | `markup()`, `render()`, `declare`, `on`, `link` | UI & interactivity |
| `%import tables` | `truthtable()` | Boolean logic tables |

```
%import console
%import app

print("Hello!")
markup("# Welcome")
render(button("Click", "primary"))
```

## 📝 Variable Types

Algolang has 5 specialized variable types:

```
let x = 10          // Mutable - can change
const PI = 3.14     // Constant - cannot change
calc area = x * x   // Calculated - expression
acc total = 0       // Accumulator - use +=
counter n = 0       // Counter - use ++ and --
```

| Type | Keyword | Operators | Use Case |
|------|---------|-----------|----------|
| Mutable | `let` | `=` | General variables |
| Constant | `const` | none | Fixed values |
| Calculated | `calc` | `=` | Computed expressions |
| Accumulator | `acc` | `+=` | Running totals |
| Counter | `counter` | `++` `--` | Counting |

## 🔁 Control Flow

### For Loops
```
for i in range(5) { print(i) }         // 0,1,2,3,4
for i in range(1, 6) { print(i) }      // 1,2,3,4,5
for i in range(0, 10, 2) { print(i) }  // 0,2,4,6,8
```

### While Loops
```
let x = 0
while x < 5 { print(x); x += 1 }
```

### Conditionals
```
if score >= 90 { print("A") }
if x > 0 { print("positive") } else { print("negative") }
```

## 🧮 Built-in Functions

### Math
| Function | Description |
|----------|-------------|
| `abs(n)` | Absolute value |
| `sqrt(n)` | Square root |
| `pow(a, b)` | Power |
| `floor(n)` `ceil(n)` `round(n)` | Rounding |
| `sin(n)` `cos(n)` `tan(n)` | Trigonometry |
| `random(a, b)` | Random integer |
| `clamp(v, min, max)` | Limit value |

### Algorithms
| Function | Description |
|----------|-------------|
| `fibonacci(n)` | Nth Fibonacci number |
| `factorial(n)` | n! |
| `isPrime(n)` | Prime check |
| `primes(n)` | Primes up to n |
| `gcd(a, b)` | Greatest common divisor |
| `lcm(a, b)` | Least common multiple |
| `binary(n)` | Convert to binary |
| `hex(n)` | Convert to hex |

### Arrays
| Function | Description |
|----------|-------------|
| `len(a)` | Length |
| `sum(a)` | Sum all |
| `avg(a)` | Average |
| `min(a)` `max(a)` | Min/Max |
| `sort(a)` | Sort ascending |
| `reverse(a)` | Reverse |
| `unique(a)` | Remove duplicates |
| `contains(a, v)` | Check membership |

### Statistics
| Function | Description |
|----------|-------------|
| `mean(a)` | Average |
| `median(a)` | Middle value |
| `stdev(a)` | Standard deviation |

### Boolean Logic
| Function | Description |
|----------|-------------|
| `AND(a, b)` | Logical AND |
| `OR(a, b)` | Logical OR |
| `NOT(a)` | Logical NOT |
| `XOR(a, b)` | Exclusive OR |
| `NAND(a, b)` | NOT AND |
| `NOR(a, b)` | NOT OR |

## 🎨 UI Components

### Markup
```
markup("# Heading 1")
markup("## Heading 2")
markup("**bold** and *italic*")
markup("`code`")
markup("> Blockquote")
```

### Components
```
render(button("Click", "primary"))
render(badge("New", "success"))
render(progress(75, 100))
render(card("Title", "Content"))
render(alert("Message", "info"))
render(table(["A","B"], [["1","2"]]))
```

### Styles
`primary` `success` `danger` `warning` `purple` `pink` `dark` `large` `small`

## 🎮 Interactive Apps

Build interactive applications with `declare`, `on`, and `link`:

```
%import app

markup("# Counter")

counter score = 0
declare disp = display(0)
declare addBtn = button("+1", "success")
declare subBtn = button("-1", "danger")

link disp to score

on addBtn { score++ }
on subBtn { score-- }
```

### Reading Input
```
declare nameInput = input("Your name", "name")
declare submitBtn = button("Submit", "primary")

on submitBtn {
  let name = getInput("name")
  print("Hello, " + name)
}

// Convert to number
let age = toNumber(getInput("age"))
```

## 🔘 Truth Tables

Generate truth tables for boolean expressions:

```
%import tables

truthtable("A AND B")
truthtable("A OR B")
truthtable("NOT A")
truthtable("(A AND B) OR C")
truthtable("A XOR B")
```

## 📚 Examples

### FizzBuzz
```
%import console

for i in range(1, 16) {
  if i % 15 == 0 { print("FizzBuzz") }
  if i % 3 == 0 { if i % 5 != 0 { print("Fizz") } }
  if i % 5 == 0 { if i % 3 != 0 { print("Buzz") } }
  if i % 3 != 0 { if i % 5 != 0 { print(i) } }
}
```

### Fibonacci Sequence
```
%import console

for i in range(0, 15) {
  print("fib(" + i + ") = " + fibonacci(i))
}
```

### Clicker Game
```
%import app

markup("# 🎮 Clicker")

counter clicks = 0
counter multiplier = 1

declare disp = display(0, "large")
declare clickBtn = button("CLICK!", "success large")
declare upgradeBtn = button("2x (50)", "purple")

link disp to clicks

on clickBtn { clicks += multiplier }
on upgradeBtn { 
  if clicks >= 50 { 
    clicks -= 50
    multiplier *= 2 
  } 
}
```

### Dashboard
```
%import app

markup("# 📊 Dashboard")
render(flex(badge("Live", "success") + badge("Today", "primary")))
render(card("Revenue", "$12,450"))
render(progress(78, 100, "success"))
render(table(["Metric", "Value"], [
  ["Visitors", "45.2k"],
  ["Signups", "1,892"],
  ["Revenue", "$12.4k"]
]))
```

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + Enter` | Run code |
| `Cmd + Enter` | Run code (Mac) |

## 🗂️ Project Structure

```
algolang/
├── algolang.html    # Single-file application (everything included)
├── README.md        # This file
└── LICENSE          # MIT License
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Inspired by educational programming languages
- Built for learning algorithms and boolean logic
- Designed with beginners in mind

---

<div align="center">

**Made with ❤️ for learners everywhere**

[⬆ Back to Top](#-algolang)

</div>

