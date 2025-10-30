# USF REU Poster Template

This repository provides a **three-column academic poster template** for the **University of South Florida (USF)** REU and undergraduate research programs.
It uses the `beamerposter` class with the Gemini theme, providing a clean and professional format suitable for symposiums, showcases, and conferences.

---

## Getting Started

1. **Download or Clone the Repository**

   Option A – *Direct download (recommended for most users)*

   * Click the green **“Code”** button at the top of this GitHub page.
   * Choose **“Download ZIP”**.
   * Extract the ZIP file on your computer.

   Option B – *Using Git (for advanced users)*

   ```bash
   git clone https://github.com/CJHRobotics/Bellini_REU_Symposium_Poster_Template.git
   ```

2. **Upload the Template to Overleaf**

   * Go to [https://www.overleaf.com](https://www.overleaf.com).
   * Click **New Project → Upload Project**.
   * Drag and drop the extracted ZIP folder or select all the files (`poster.tex`, `poster.bib`, `figures/`, and `logos/`).
   * Overleaf will import everything and set up the project automatically.
   * Press **Recompile** to generate your poster PDF.

3. **Edit the Template**

   * Open `poster.tex`.
   * Look for comments marked **`STUDENT EDIT HERE`** — these indicate where you should make changes.
   * Replace the sample text, add your own figures, and cite references from `poster.bib`.
   * Do not modify layout or formatting code.

---

## File Structure

```
project/
│
├── poster.tex              # Main LaTeX source file
├── poster.bib              # Reference file (BibLaTeX format)
├── figures/                # Folder for your figures and charts
│   ├── example.png
│   └── learning_curve_example.png
├── logos/                  # Folder for USF logo and QR code (optional)
│   ├── usflogo.png
│   └── qr.png
└── README.md               # Instructions and usage guide
```

---

## Writing the Poster

Each section of the poster is preformatted and includes instructions as comments in the LaTeX file.

### Abstract

Write a 150–250 word paragraph summarizing the purpose, methods, key findings, and importance of your work. Avoid figures, equations, or citations.

### General Project Description and Goals

Describe the motivation and background for your research. Include 2–4 clear, measurable goals.

### Experiments and Results

Summarize the experimental setup and methods. Include tables and figures with captions:

```latex
\caption{Results comparing three experimental conditions.}
\label{tab:results_demo}
```

To reference these in text:

```latex
See Table~\ref{tab:results_demo}.
```

### Discussion

Interpret your results. Use **bold**, *italics*, and \underline{underlining} sparingly for emphasis.
Reference tables and figures (e.g., *As shown in Fig.~\ref{fig:summary_plot}...*).

### Future Work and Acknowledgments

List actionable next steps and credit mentors, collaborators, or funding sources such as NSF grants.

### References

Add citations in `poster.bib` using BibLaTeX. Example:

```bibtex
@article{doe2024,
  author  = {Doe, Jane and Smith, Alex},
  title   = {Learning Visual Place Cells in Robots},
  journal = {Frontiers in Neurorobotics},
  year    = {2024}
}
```

---

## Compiling the Poster

### On Overleaf

* Press **Recompile** to build the poster.
* The project uses **PDFLaTeX** with BibLaTeX; no extra configuration is needed.

### Locally (Optional)

If you want to compile locally using TeXLive:

```bash
pdflatex poster.tex
biber poster
pdflatex poster.tex
pdflatex poster.tex
```

---

## Final Checklist Before Submission

* [ ] Replace all placeholder text marked with `STUDENT EDIT HERE`.
* [ ] Ensure all images load correctly from the `figures/` directory.
* [ ] Verify all references appear at the end.
* [ ] Check for spelling, clarity, and alignment consistency.
* [ ] Export as an **A2 landscape PDF** for printing or submission.

---

## License

This template is released under the **MIT License (2025)**
Copyright © 2025 **Chance J. Hamilton**

Permission is granted to use, copy, modify, and distribute this template for educational and research purposes with attribution.


