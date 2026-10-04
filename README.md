#  GTU SPI Calculator

A mobile-friendly SPI (Semester Performance Index) calculator for **Gujarat Technological University** students, built as a single HTML file with zero dependencies.

> **Live Demo →** [jayvegada.github.io/gtu-spi-calculator](https://jayvegada.github.io/gtu-spi-calculator/)

---

##  Features

### Two clearly separated modes

| Mode | Use it when | What it does |
| ---- | ----------- | ------------ |
| **Actual SPI** | *"I know my marks."* | Calculates your actual SPI from the marks you entered. Nothing is predicted, and blank marks stay **Pending** (never counted as 0). |
| **Expected SPI** | *"I don't know my GTU ESE marks yet."* | You set a Target SPI, enter the marks you already have (Mid/PA, internal, viva…), and choose an **Expected Final Grade** for each pending subject. The calculator shows the **GTU ESE marks required** and **simulates** the resulting **Expected SPI**. |

**How the Expected SPI simulation works**

```
Expected Final Grade (e.g. BB)
  → GTU ESE Required (e.g. 45 / 70)
  → temporary simulated ESE mark on a copy of the subject
  → same Final Subject Grade logic as Actual mode (BB)
  → Grade Point (8)
  → Expected SPI (combined across all selected subjects)
```

- The Expected Final Grade is the **Final Subject Grade** used for SPI, **not** the GTU ESE component grade. `45 / 70` is a *mark*, not a grade.
- It is a planning simulation only. Your entered marks and your Actual SPI are **never modified**.
- If the requirement is a range, the minimum mark of the range is simulated (a conservative simulation, not an official threshold). If it is impossible or needs missing information, nothing is invented.
- The Expected SPI shows the real simulated result. It is not forced to equal the Target SPI, and the app tells you whether the target is achievable.

### Calculator

- **Official GTU Teaching Scheme data**: structure comes from **subject code + effective year** (E / M / I / V marks), with no marks pre-filled
- **Semester presets**: CE Sem 1, 2, 3, 4, 5 and Custom
- **Semester 5**: core subjects plus elective dropdowns (Professional Elective-I, II, Multidisciplinary Open Elective); changing an elective swaps it in place with no duplicates
- **Custom subjects**: Theory 100, Theory + Practical 150 / 200, Theory + PBL 130, Theory + Internal 120, Theory + Viva 170, or Blank / Full Custom
- **Grade-based entry**: enter a letter grade (AA, AB…) and it is treated as a mark *range*, never a made-up mark
- **Marksheet override**: paste the Final Subject Grade from your official marksheet and it is used as-is (including `PS` for non-credit subjects)
- **Pass/fail detection** per component
- **Help & Calculation Guide**: grade tables, worked examples, and an explanation of both modes
- **Share your marks** (WhatsApp / SMS / copy), **Save & Load** presets, **auto-save**, **dark / light theme**
- **Responsive**: checked from 320px phones to 1440px desktops, with no page-level horizontal scrolling
- **100% offline**: no server, no login, no data sent anywhere

---

##  How the Grade Is Calculated

The calculator keeps four levels separate. **Only the Final Subject Grade becomes a grade point and enters SPI.**

| Step | What it is | Example |
| ---- | ---------- | ------- |
| 1. Component Grade | One part (ESE, Mid/PA, practical) on its own table | ESE 45/70 → BB |
| 2. Theory / Practical Total | Marks of that part added, then graded | 45 + 20 = 65/100 → BB |
| 3. **Final Subject Grade** | All counted marks pooled, then graded | 162/200 = 81% → AB |
| 4. Grade Point | Number for the Final Subject Grade | AB = 9, × 4 credits = 36 |

```
SPI = Σ(Grade Point × Credits) / Σ(Credits)
```

### Grade table

| Grade | Points | Min % |
| ----- | ------ | ----- |
| AA | 10 | 85% |
| AB | 9 | 75% |
| BB | 8 | 65% |
| BC | 7 | 55% |
| CC | 6 | 45% |
| CD | 5 | 40% |
| DD | 4 | 35% |
| FF | 0 | < 35% |

### Component tables

| Grade | ESE (out of 70) | Mid / PA (out of 30) |
| ----- | --------------- | -------------------- |
| AA | 60–70 | 26–30 |
| AB | 52–59 | 23–25 |
| BB | 45–51 | 20–22 |
| BC | 38–44 | 17–19 |
| CC | 31–37 | 15–16 |
| CD | 27–30 | 13–14 |
| DD | 23–26 | 12 |
| FF | 0–22 | 0–11 |

### Subject structure (E / M / I / V)

| Teaching Scheme | Calculator component |
| --------------- | -------------------- |
| E: External Theory | GTU ESE |
| M: Internal Assessment | Theory PA |
| V: External Viva | External Viva |
| I: Internal Viva / Submission | Practical PA |

The structure depends on the **subject code and its effective year**. For example, Physics is 70/30/20/30 = 150 in the 2024-25 row but 70/30/50/50 = 200 in 2025-26.

---

##  Important: Estimate, Not an Official Formula

The required exam-mark estimate uses the available subject structure and a **pooled-mark model**. This is strongly consistent with the available GTU results (it fits every real subject on the Sem 1–4 marksheets used for testing), but **GTU has not publicly stated this exact final-subject-grade formula** in the materials used here. Therefore the required ESE mark is an **estimate, not an official GTU guarantee**.

The E/M/I/V → marksheet-column mapping is likewise a working assumption. If you have your marksheet's Final Subject Grade, enter it on the subject to use the official value.

---

##  How to Use

**Online:** open the live demo link above. No installation needed.

**Locally:**

```bash
git clone https://github.com/JayVegada/gtu-spi-calculator.git
# open index.html in any browser. That's it.
```

### Quick start

1. Pick a template (**CE Sem 1–5** or **Custom**).
2. **Actual SPI:** enter the marks you have and read your SPI.
3. **Expected SPI:** set a Target SPI, leave the GTU ESE blank, choose an Expected Final Grade per pending subject, and read the required ESE and Expected SPI.
4. Use **Save** to keep your setup, **Share** to send a summary, **Help** for the full guide.

---

##  Testing

The app runs a built-in self-test suite on load (**118 checks**) covering grade tables, the Teaching Scheme data, SPI regression against real Sem 1–4 marksheets, the pooled-mark model, target and expected-grade simulation, Save/Load migration of old saves, and Sem 5 elective handling. Results are printed to the browser console as `[GTU SPI self-test]`.

---

##  Tech Stack

| What | How |
| ---- | --- |
| Structure | Plain HTML5 |
| Styling | CSS3 with custom properties (no framework) |
| Logic | Vanilla JavaScript (no libraries) |
| Storage | Browser `localStorage` |
| Fonts | Google Fonts (Inter, Source Serif 4, Plus Jakarta Sans, JetBrains Mono) |

Single file. No build step. No npm. No framework.

---

##  Project Structure

```
gtu-spi-calculator/
├── index.html      # The entire app
├── README.md
└── LICENSE
```

---

##  Limitations

- Only **Computer Engineering Sem 1–5** have official data; Sem 6–8 are not included because official data isn't available yet.
- NPTEL / MOOC electives (100-mark scoring) don't fit the E/M/I/V model; use **Custom → Theory 100** for those.
- The Final Subject Grade is a pooled-mark **estimate** unless you enter the marksheet grade.

---

##  Contributing

Pull requests are welcome. Ideas:

- Teaching Scheme data for other branches (Mech, Civil, EC, IT…)
- Sem 6–8 once official data is available
- CPI calculator (across semesters)
- Export result as PDF or image
- PWA support (installable on phone)

---

##  License

MIT License. See [LICENSE](https://github.com/JayVegada/gtu-spi-calculator/blob/main/LICENSE).

---

##  Author

**Jay Vegada**

- GitHub: [@JayVegada](https://github.com/JayVegada)
- LinkedIn: [in/jay-vegada-ja045y](https://www.linkedin.com/in/jay-vegada-ja045y/)

---

> Made for GTU students, by a GTU student. ⚡
