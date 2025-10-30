# USF REU Poster Template (Beamerposter + Gemini Theme)

This Overleaf project provides a **three-column academic poster template** for the University of South Florida’s REU and undergraduate research programs.
It uses the `beamerposter` class with the Gemini theme, providing a clean, readable layout suitable for academic presentations and symposia.

---

## Getting Started

1. **Open `poster.tex`**
   This is the main file where all poster content is written and organized.

2. **Locate the comments marked with `STUDENT EDIT HERE`**
   These comments identify areas that you should modify:

   * Title, author names, and affiliations
   * Abstract and project description
   * Figures, tables, and captions
   * Discussion, acknowledgments, and references

3. **Avoid changing the structure or formatting code**
   The layout, color scheme, and spacing have already been optimized.
   Focus on adding and editing text content.

---

## File Structure

```
project/
│
├── poster.tex              # Main LaTeX source file
├── poster.bib              # Bibliography file (BibLaTeX format)
├── figures/                # Folder for all images
│   ├── example.png
│   └── learning_curve_example.png
├── logos/                  # Folder for logos or QR codes
│   ├── usflogo.png
│   └── qr.png
└── README.md               # Instructional guide
```

---

## Writing the Poster Sections

### Abstract

* Write one paragraph (150–250 words).
* Describe the **problem**, **method**, **key findings**, and **importance**.
* Avoid figures, tables, or citations.
* Keep language accessible for a general STEM audience.

### General Project Description and Goals

* Explain **why** the project is important and **what** it aims to achieve.
* Include 2–4 concise, measurable goals.
* Use short paragraphs and bullet points for clarity.

### Experiments

* Outline what was tested, how data was collected, and which metrics were used.
* Mention independent and dependent variables clearly.
* Keep this section factual and structured.

### Results

* Present findings in a clear format such as a table or figure.
* Include labels and captions for every table and figure.
* Example:

  ```latex
  \caption{Performance results across multiple test configurations.}
  \label{tab:results_demo}
  ```
* When referring to your table in text, use:

  ```latex
  See Table~\ref{tab:results_demo}.
  ```

### Discussion

* Interpret your results and connect them to the project goals.
* Do not repeat raw numbers or re-describe figures.
* Use **bold**, *italics*, and \underline{underlining} sparingly to emphasize ideas.
* Example reference:

  ```latex
  As shown in Fig.~\ref{fig:summary_plot}, higher cluster counts produced more stable results.
  ```

### Future Work

* List 2–4 specific steps for continuing the project.
* Examples: testing on hardware, expanding datasets, or integrating new algorithms.

### Acknowledgments

* Recognize supporting grants, mentors, or collaborators.
* Example:

  > This material is based upon work supported by the National Science Foundation under Grant No. XXXXXXX.

### References

* All sources should be listed in `poster.bib` using BibTeX format.
* Example entry:

  ```bibtex
  @article{doe2024,
    author  = {Doe, Jane and Smith, Alex},
    title   = {Learning Visual Place Cells in Robots},
    journal = {Frontiers in Neurorobotics},
    year    = {2024}
  }
  ```
* Cite references using:

  ```latex
  \cite{doe2024}
  ```

---

## Adding Figures

1. Place image files in the `/figures` directory.
2. Include them with:

   ```latex
   \includegraphics[width=0.7\linewidth]{figures/my_image.png}
   ```
3. Adjust the width to control image size (`0.5\linewidth` to `\linewidth`).
4. Always include a caption and label for each figure.

---

## Compiling the Poster

### In Overleaf

* Press **Recompile** to build the PDF.
* The default compiler (PDFLaTeX) is sufficient.

### On a Local Machine

If compiling locally, run the following commands:

```bash
pdflatex poster.tex
biber poster
pdflatex poster.tex
pdflatex poster.tex
```

This sequence ensures that all citations and references appear correctly.

---

## Final Checklist Before Submission

* [ ] Replace all placeholder text marked with `�� STUDENT EDIT HERE`.
* [ ] Verify that all figures load correctly and are properly labeled.
* [ ] Confirm that all references appear at the end of the poster.
* [ ] Check for spelling, clarity, and alignment consistency.
* [ ] Export the final version as **A2 landscape PDF** for printing.

---

## Additional Advice

* Keep text concise.
* Avoid large paragraphs; prefer bullets and short sentences.
* Use color contrast wisely and ensure figures are legible from a distance.
* Verify that each figure or table directly supports a key claim in your discussion.
* Always proofread your final version carefully.
