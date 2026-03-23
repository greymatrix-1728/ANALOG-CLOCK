# 🕐 Analog Clock

A real-time analog clock built with pure HTML, CSS, and JavaScript — no libraries, no frameworks.

---

## 🌐 Live Demo
> Open `index.html` in any browser to run the project locally.

---


## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure of the clock |
| CSS3 | Styling, positioning of clock hands |
| JavaScript (Vanilla) | Real-time logic and hand rotation |

---

## ✨ Features

- ✅ Real-time working analog clock
- ✅ Displays live **Hours, Minutes, and Seconds**
- ✅ Smooth hand rotation using CSS `transform`
- ✅ Fully **responsive** — scales with screen size using `vw` units
- ✅ Clean UI with a clock face background image
- ✅ Zero dependencies — pure HTML, CSS, JS

---

## 📁 Project Structure

```
analog-clock/
│
├── index.html       # Main HTML structure
├── index.css        # Styling and positioning of clock hands
├── index.js         # JavaScript logic for real-time clock
├── clock.png        # Clock face background image
└── README.md        # Project documentation
```

---

## ⚙️ How It Works

### HTML
- A `#clockContainer` div acts as the clock face
- Three divs inside it represent the **hour**, **minute**, and **second** hands

### CSS
- `#clockContainer` uses `position: relative` as the anchor
- All three hands use `position: absolute` to place them at the **center of the clock**
- `transform-origin: bottom` makes hands **rotate from their base** (like a real clock)
- Percentage-based sizing makes the clock **fully responsive**

### JavaScript
- `setInterval()` runs every **1000ms (1 second)**
- Gets current time using `new Date()`
- Calculates rotation angles:

| Hand | Formula | Reason |
|------|---------|--------|
| Hour | `30 × hours + minutes / 2` | 360° ÷ 12 = 30° per hour |
| Minute | `6 × minutes` | 360° ÷ 60 = 6° per minute |
| Second | `6 × seconds` | 360° ÷ 60 = 6° per second |

- Applies rotation via `element.style.transform = rotate(Xdeg)`

---

## 🚀 How to Run Locally

1. Clone the repository:
```bash
git clone https://github.com/your-username/analog-clock.git
```

2. Navigate into the folder:
```bash
cd analog-clock
```

3. Open `index.html` in your browser:
```bash
# Either double click index.html
# Or use Live Server in VS Code
```

---

## 📚 Concepts Used

- CSS `position: absolute` and `position: relative`
- CSS `transform` and `transform-origin`
- CSS `vw` units for responsiveness
- JavaScript `Date` object
- JavaScript `setInterval()`
- DOM manipulation via `element.style`

---

