# SO-22 Bank Exam — Result Analysis

**Live Demo → [plabonkumersarker.github.io/so22-ratio](https://plabonkumersarker.github.io/so22-ratio)**

A single-page interactive analysis tool for the **Senior Officer (General) — SO-22** Bangladesh bank job exam. It visualizes the journey of every candidate across three stages — Written, Viva, and Final Selection — and plots a competition ratio hypothesis for each viva group.

---

## What It Does

Every candidate who appeared in the SO-22 written exam is displayed as a color-coded button:

| Color | Meaning |
|-------|---------|
| 🔘 **Grey** | Appeared in written exam — not called for viva |
| 🟢 **Green** | Passed written, attended viva — not finally selected |
| 🟠 **Orange** | Passed written, passed viva — finally selected |

Click any button (or search by roll number) to see that candidate's full status, viva group details, and their competition ratio.

---

## Features

- **Search by roll number** — instantly highlights and opens a detail modal
- **Detail modal** — shows written status, viva status, final result, selected bank, merit position, and ratio
- **Competition ratio** — for each viva group: `written candidates in roll range ÷ viva candidates`
- **Overall ratio distribution chart** — bar chart grouping all viva groups by ratio range
- **Bank-wise scatter charts** — one chart per bank, showing each selected candidate's merit position vs ratio
- **All-candidates chart** — all 974 selected candidates on one wide scrollable canvas, color-coded by bank
- **Dark / Light theme toggle** — defaults to dark, one-click switch
- **Visitor counter** — live session-deduplicated visit count
- **Scroll button** — direction-aware (↑ when scrolling up, ↓ when scrolling down)

---

## Data

| Dataset | Count |
|---------|-------|
| Candidates appeared in written | 7,805 |
| Called for viva | 3,205 |
| Finally selected | 974 |
| Banks | 9 |
| Viva groups | 54 |

### Banks Covered

- Sonali Bank PLC (414 selected)
- Agrani Bank PLC (250 selected)
- Janata Bank PLC (100 selected)
- Bangladesh Krishi Bank (68 selected)
- Rajshahi Krishi Unnayan Bank (60 selected)
- Bangladesh Development Bank PLC (40 selected)
- Probashi Kallyan Bank (20 selected)
- Karma Sangsthan Bank (12 selected)
- Bangladesh House Building Finance Corporation (10 selected)

---

## The Ratio Hypothesis

> **Ratio = Written candidates in roll range ÷ Viva candidates in that group**

Each viva session calls a batch of candidates within a specific roll number range. The ratio compares how many people from the written list fall in that range against how many were actually called for viva. A higher ratio means more competition within that group.

*This is a community hypothesis — treat it as an interesting data point, not a definitive metric.*

---

## Stack

Built as a single self-contained HTML file — no framework, no backend, no build step.

- Vanilla JavaScript (ES5 compatible)
- [Chart.js 4.4](https://www.chartjs.org/) — bar and scatter charts
- [Google Fonts](https://fonts.google.com/) — Sora + Space Mono
- CSS custom properties for dark/light theming
- [CountAPI](https://countapi.mileshilliard.com/) — visitor counter

---

## Project Structure

```
so22-ratio/
├── index.html      # Entire application (data + logic + styles)
└── README.md
```

All candidate data is embedded directly in the HTML — no external data files or API calls required (except the visitor counter).

---

## Running Locally

No build step needed. Just open the file:

```bash
git clone https://github.com/plabonkumersarker/so22-ratio.git
cd so22-ratio
open index.html   # macOS
# or double-click index.html in your file manager
```

Or serve it locally:

```bash
npx serve .
# then open http://localhost:3000
```

---

## Deploying to GitHub Pages

1. Push `index.html` and `README.md` to the `main` branch
2. Go to **Settings → Pages**
3. Set source to **Deploy from a branch → main → / (root)**
4. Your site will be live at `https://plabonkumersarker.github.io/so22-ratio`

---

**Ratio Hypothesis** — [Thohidul Islam Riad](https://www.facebook.com/share/1GidotutT9/)

**Development** — [Plabon Kumer Sarker](https://plabonkumersarker.github.io/profile)

---

*Data sourced from official SO-22 exam results. This tool is for informational and analytical purposes only.*
