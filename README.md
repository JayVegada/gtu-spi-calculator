# 🎓 GTU SPI Calculator

A smart, mobile-friendly SPI (Semester Performance Index) calculator for **Gujarat Technological University** students — built as a single HTML file with zero dependencies.

> **Live Demo →** [jayvegada.github.io/gtu-spi-calculator](https://jayvegada.github.io/gtu-spi-calculator/GTU-SPI-CALCULATOR.html)

---

## ✨ Features

- **All 6 GTU subject types** — T+P 200, T+P 150, T+P 130, T+P 120, Theory 100, Theory 80, No GTU (internal-only)
- **Target SPI prediction** — Set your target SPI and see exactly how many marks you need in the GTU exam
- **Grade-based entry** — Enter marks as letter grades (AA, AB, BB…) instead of raw numbers
- **Estimated grade picker** — Blank the GTU exam field → pick an expected grade → instantly preview your SPI
- **Pass/fail detection** — Warns you per-component if you're below the GTU pass threshold
- **Save & Load presets** — Name and store subject configurations in your browser (localStorage)
- **Auto-save** — Your session is automatically restored when you reopen the page
- **Dark / Light theme** — Toggleable, remembers your preference
- **Mobile-first design** — Works great on phones, tablets, and desktops
- **100% offline** — No server, no login, no data sent anywhere

---

## 📸 Screenshots

> *(Add your screenshots here)*

| Dark Mode | Light Mode |
|-----------|------------|
| ![dark](screenshots/dark.png) | ![light](screenshots/light.png) |

---

## 🚀 How to Use

### Option 1 — Use Online (GitHub Pages)
Just open the live demo link above. No installation needed.

### Option 2 — Run Locally
```bash
# Clone the repo
git clone https://github.com/JayVegada/gtu-spi-calculator.git

# Open in browser — that's it!
open GTU-SPI-CALCULATOR.html
```

---

## 📚 GTU Grade Table

| Grade | Points | Min % |
|-------|--------|-------|
| AA    | 10     | 85%   |
| AB    | 9      | 75%   |
| BB    | 8      | 65%   |
| BC    | 7      | 55%   |
| CC    | 6      | 45%   |
| CD    | 5      | 40%   |
| DD    | 4      | 35%   |
| FF    | 0      | < 35% |

**SPI Formula:**
```
SPI = Σ(Grade Points × Credits) / Σ(Credits)
```

---

## 🗂️ Subject Type Presets

| Preset      | GTU ESE | Mid Exam | Internal/Practical | Total |
|-------------|---------|----------|--------------------|-------|
| T+P 200     | 70      | 30       | 100                | 200   |
| T+P 150     | 70      | 30       | 20 + 30 (Viva)     | 150   |
| T+P 130     | 70      | 30       | 30                 | 130   |
| T+P 120     | 70      | 30       | 20                 | 120   |
| Theory 100  | 70      | 30       | —                  | 100   |
| Theory 80   | 50      | 30       | —                  | 80    |
| No GTU      | —       | 30       | 20                 | 50    |

---

## 💡 Tips

- **Leave GTU exam marks blank** to activate target prediction mode
- Tap **🎯** on any component to mark it as the "exam component" for SPI targeting
- Use **CE Sem 4** template to load a pre-filled example with 6 subjects
- **Save presets** with your subject structure so you don't have to set it up each semester

---

## 🛠️ Tech Stack

| What | How |
|------|-----|
| Structure | Plain HTML5 |
| Styling | CSS3 with custom properties (no framework) |
| Logic | Vanilla JavaScript (no libraries) |
| Storage | Browser `localStorage` |
| Fonts | Google Fonts (Inter, Plus Jakarta Sans, JetBrains Mono) |

Single file. No build step. No npm. No framework.

---

## 📁 Project Structure

```
gtu-spi-calculator/
├── GTU-SPI-CALCULATOR.html  # The entire app
├── README.md
├── LICENSE
└── screenshots/             # Optional — add your own
    ├── dark.png
    └── light.png
```

---

## 🤝 Contributing

Pull requests are welcome! Some ideas if you want to contribute:

- Add more branch-specific semester templates (Mech, Civil, EC, IT…)
- CPI calculator (across semesters)
- Export result as PDF or image
- PWA support (installable on phone)

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

## 👤 Author

**Jay Vegada**
- GitHub: [@JayVegada](https://github.com/JayVegada)
- LinkedIn: [in/jay-vegada-ja045y](https://www.linkedin.com/in/jay-vegada-ja045y/)

---

> Made for GTU students, by a GTU student. ⚡

