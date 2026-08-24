# 🎓 GTU SPI Calculator

A smart, mobile-friendly SPI (Semester Performance Index) calculator for **Gujarat Technological University** students — built as a single HTML file with zero dependencies.

> **Live Demo →** [jayvegada.github.io/gtu-spi-calculator](https://jayvegada.github.io/gtu-spi-calculator/)

---

## ✨ Features

- **17 GTU subject-type templates** — CE Sem 1–4 (full pre-filled semesters), T+P 200, T+P 200 II, T+P 170, T+P 150, T+P 130, T+P 120, Theory 100, Theory 80, Constitution, No GTU, Pure Internal, Project, and Custom
- **Target SPI prediction** — Set your target SPI and see exactly how many marks you need in the GTU exam
- **Grade-based entry** — Enter marks as letter grades (AA, AB, BB…) instead of raw numbers
- **Estimated grade picker** — Blank the GTU exam field → pick an expected grade → instantly preview your SPI
- **Pass/fail detection** — Warns you per-component if you're below the GTU pass threshold
- **Built-in Guide** — A one-tap "How to Use" modal explaining SPI, grades, components, and targeting — no more guessing
- **Share your marks** — Generate a shareable text summary and send it straight to WhatsApp, SMS, or wherever, or copy it to your clipboard
- **Save & Load presets** — Name and store subject configurations in your browser (localStorage)
- **Auto-save** — Your session is automatically restored when you reopen the page
- **Dark / Light theme** — Toggleable, remembers your preference
- **Dynamic design** — Works great on phones, tablets, and desktops
- **100% offline** — No server, no login, no data sent anywhere

---

## 🚀 How to Use

### Option 1 — Use Online (GitHub Pages)
Just open the live demo link above. No installation needed.

### Option 2 — Run Locally
```bash
# Clone the repo
git clone https://github.com/JayVegada/gtu-spi-calculator.git

# Open in browser — that's it!
open index.html
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

| Preset       | GTU ESE | Mid Exam | Internal/Practical            | Total |
|--------------|---------|----------|--------------------------------|-------|
| T+P 200      | 70      | 30       | 100                            | 200   |
| T+P 200 II   | 70      | 30       | 20 + TW/SL 30 + Viva 50        | 200   |
| T+P 170      | 70      | 30       | 20 + Viva 50                   | 170   |
| T+P 150      | 70      | 30       | 20 + 30 (Viva)                 | 150   |
| T+P 130      | 70      | 30       | 30                              | 130   |
| T+P 120      | 70      | 30       | 20                              | 120   |
| Theory 100   | 70      | 30       | —                               | 100   |
| Theory 80    | 50      | 30       | —                               | 80    |
| Constitution | 50      | —        | Internal (PBL) 30              | 80    |
| No GTU       | —       | 30       | 20                              | 50    |
| Pure Internal| —       | —        | Internal 100                   | 100   |

**Full-semester templates** — **CE Sem 1**, **CE Sem 2**, **CE Sem 3**, and **CE Sem 4** load an entire pre-filled semester (all subjects, credits, and components) in one tap, matching the actual GTU Computer Engineering syllabus.

---

## 💡 Tips

- **Leave GTU exam marks blank** to activate target prediction mode
- Tap **🎯** on any component to mark it as the "exam component" for SPI targeting
- Use the **CE Sem 1–4** templates to load a full pre-filled semester in one tap
- Open the **❓ Guide** in the top bar any time for a refresher on how everything works
- **Save presets** with your subject structure so you don't have to set it up each semester
- Use **📤 Share** to send a quick summary of your marks to friends over WhatsApp

---

## 🛠️ Tech Stack

| What | How |
|------|-----|
| Structure | Plain HTML5 |
| Styling | CSS3 with custom properties (no framework) |
| Logic | Vanilla JavaScript (no libraries) |
| Storage | Browser `localStorage` |
| Fonts | Google Fonts (Inter, Source Serif 4, Plus Jakarta Sans, JetBrains Mono) |

Single file. No build step. No npm. No framework.

---

## 📁 Project Structure

```
gtu-spi-calculator/
├── index.html         # The entire app
├── README.md
├── LICENSE
└── screenshots/        # Optional — add your own
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
