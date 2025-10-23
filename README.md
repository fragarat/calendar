# README — LaTeX Template: 2025 Calendar (with Week Numbers)

**Description**

This repository contains a LaTeX template for generating a **2025** yearly calendar that includes **ISO week numbers**. The template is designed to be clean, modular, and easy to customize (language, layout, color themes, highlighting holidays, etc.).

---

## Contents

* `2025.tex` — Main LaTeX template file.
* `README.md` — This document.
* `2025.pdf` — Main PDF template file.

---

## Requirements

To compile the template, you need a full LaTeX distribution (e.g., TeX Live or MikTeX) with at least the following packages installed:

* `pgf` / `tikz` — for drawing and date management (`pgfcalendar`).
* `datetime2` (or equivalent date utilities) — used to compute and display ISO week numbers.
* `babel` or `polyglossia` — for multilingual support.
* `fontenc`, `inputenc` (for pdfLaTeX) or XeLaTeX/LuaLaTeX with UTF-8 (recommended for accented characters).
* `xcolor`, `geometry`, `calc`, and `fancyhdr` — for layout and color customization.

> Note: The `.tex` file contains inline comments indicating which packages are required. If something is missing, install it using your LaTeX package manager.

---

## Compilation

Recommended (UTF-8 and system fonts):

```bash
xelatex calendar2025.tex
xelatex calendar2025.tex
```

Alternatively, using `pdflatex` (ensure UTF-8 encoding is enabled):

```bash
pdflatex calendar2025.tex
pdflatex calendar2025.tex
```

Run the compiler **twice** to ensure correct references and week numbering.

---

## Quick Customization Guide

The template is organized and commented for quick editing:

1. **Language:** Change the language option in `babel` (e.g., `\usepackage[english]{babel}`) or use `polyglossia` for XeLaTeX.
2. **Week start day:** By default, the calendar starts on **Monday** (ISO standard). You can change it to Sunday by adjusting the `pgfcalendar` settings.
3. **Week numbers:** ISO week numbers are displayed in a side margin or column. To hide them, disable the `showweeknumbers` option.
4. **Date and month format:** Adjust font size, alignment, or color in the style section.
5. **Holidays/special dates:** Add holidays manually in the “holiday list” section, or highlight ranges (vacations, events) using background colors.
6. **Style customization:** Change color palette, fonts, or margins in the preamble.

---

## Examples of Customization

* **Change main color:**

  ```latex
  % In the preamble
  \definecolor{main}{HTML}{1F77B4}
  ```

* **Hide week numbers:**

  ```latex
  % In the configuration section
  \def\showweeknumbers{0}
  ```

* **Add holidays:**

  ```latex
  % In the holiday list
  \newcommand{\holidays}{ {2025-01-01}, {2025-04-18}, {2025-12-25} }
  ```

---

## Contact

If you’d like help customizing the template (e.g., adding your logo, regional holidays, or a specific design), feel free to reach out for assistance.

Enjoy creating your 2025 calendar with week numbers included!

