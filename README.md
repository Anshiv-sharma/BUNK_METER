# 🎓 Bunk Meter

**Your attendance survival calculator.**

Bunk Meter is a simple, lightweight web app that helps students figure out how many classes they can skip without falling below their required attendance percentage, or how many consecutive classes they need to attend to get back on track.

No spreadsheets. No mental maths. Just enter your numbers and let Bunk Meter do the worrying.

## ✨ Features

- **Instant attendance calculation:** See your current attendance percentage.
- **Safe bunk count:** Find out how many upcoming classes you can skip while staying at or above your attendance target.
- **Attendance recovery:** If you're below the target, calculate how many consecutive classes you need to attend to reach it.
- **Custom attendance requirement:** Defaults to **75%**, but you can enter your own target.
- **Minimal, responsive interface:** Works in a browser on desktop or mobile.
- **Zero dependencies:** Pure HTML, CSS, and JavaScript.

## 🛠️ Tech Stack

| Technology | Purpose |
| --- | --- |
| HTML | Page structure and inputs |
| CSS | Styling and responsive layout |
| JavaScript | Attendance calculations and results |

## 🚀 Getting Started

1. Download or clone this repository.
2. Open `index.html` in any modern web browser.
3. Enter the number of classes you've attended, the total classes held, and your required attendance percentage.
4. Click **Check** to see your result.

No installation, build step, or server required.

## 🧮 How It Works

Let:
- `A` = classes attended
- `T` = total classes held
- `R` = required attendance percentage expressed as a decimal (e.g., `0.75` for 75%)

**Current attendance**

```text
Attendance % = (A / T) × 100
```

**If you're at or above the target:**

```text
Classes you can skip = floor(A / R - T)
```

**If you're below the target:**

```text
Classes to attend consecutively = ceil((R × T - A) / (1 - R))
```

The calculations assume every upcoming class counts equally and that the attendance target is between 0% and 100% (exclusive).

### Example

You've attended **40 out of 50 classes**, and your college requires **75% attendance**.

- Current attendance: **80%**
- Classes you can skip: **3**

If you've attended **30 out of 50 classes** instead:

- Current attendance: **60%**
- Consecutive classes needed to reach 75%: **30**

## 📁 Project Structure

```text
bunk-meter/
├── index.html    # HTML, CSS, and JavaScript
└── README.md     # Project documentation
```

## ⚠️ Notes

Bunk Meter is a planning tool. Actual attendance rules may vary by institution, and rounding or exemptions can affect official records. The current implementation checks basic input validity but does not fully validate all edge cases, such as negative values or targets of 0% and 100%.

## 📄 License

No license has been specified yet.

---

**Calculate your attendance. Plan your bunks.** 🎯
