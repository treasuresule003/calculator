# scientific-calculator
# Scientific Calculator 🧮

A sleek, retro-instrument styled scientific calculator built with pure HTML, CSS, and JavaScript. No frameworks, no dependencies, no build tools — just open it in a browser and go.

![HTML](https://img.shields.io/badge/HTML-100%25-orange)
![No Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)
![Docker](https://img.shields.io/badge/docker-ready-blue)

## ✨ Features

- **Standard operations** — addition, subtraction, multiplication, division, parentheses, percentages
- **Scientific functions** — sin, cos, tan (with inverse trig via 2nd), log, ln, square root, cube root, powers (xʸ), factorial (x!), reciprocal (1/x), absolute value, π, e, EXP
- **DEG / RAD toggle** for accurate trig calculations
- **Memory functions** — M+, M−, MR, MC
- **Ans key** to reuse your last result
- **Full keyboard support** — type numbers, operators, press Enter to calculate, Backspace to delete, Escape to clear
- **Smart parentheses handling** — automatically closes any unmatched parentheses when you hit equals
- **Safe custom parser** — expressions are evaluated with a hand-built recursive-descent parser, not `eval()`
- **Retro instrument aesthetic** — glowing CRT-style display, tactile button styling, scrolling history tape

## 🛠️ Tech Stack

Pure **HTML, CSS, and JavaScript**. No frameworks, no build step, no external JS libraries.

## 🚀 Getting Started

### Run locally

Just open the file directly in your browser:

```bash
open calculator.html      # macOS
xdg-open calculator.html  # Linux
start calculator.html     # Windows
```

Or serve it with a simple local server:

```bash
python3 -m http.server 8080
```
Then visit `http://localhost:8080/calculator.html`

### Run with Docker

This project includes a `Dockerfile` that serves the calculator using nginx.

**Build the image:**
```bash
docker build -t scientific-calculator .
```

**Run the container:**
```bash
docker run -d -p 8080:80 --name sc7-calculator scientific-calculator
```

**Open in your browser:**

http://localhost:8080


**Stop and remove the container:**
```bash
docker stop sc7-calculator
docker rm sc7-calculator
```

## 📁 Project Structure

.
├── calculator.html # Complete app — markup, styling, and logic
├── Dockerfile # nginx-based container setup
└── README.md # This file


## 🧠 How It Works

- All calculations happen entirely client-side — no data ever leaves your browser
- Trigonometric functions respect the DEG/RAD mode shown on screen
- Factorial (x!) computes exact results for whole numbers and uses a Lanczos gamma-function approximation for non-integer inputs
- Input is tokenized and parsed with a custom recursive-descent parser for safe, predictable evaluation

## 📄 License

Feel free to use, modify, and share this project.
