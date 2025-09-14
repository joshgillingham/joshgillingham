## Resume/CV LaTeX Project

This repository contains LaTeX source files for building your resume, CV, and cover letter using the `awesome-cv` class.

### Building the Documents

To build the PDF files (e.g., `resume.pdf`, `cv.pdf`, `coverletter.pdf`), you need a working LaTeX environment with all required packages.

#### Prerequisites (macOS)

1. **Install TeX Live** (recommended: full version for fewer missing packages):
   Using Homebrew:
     ```sh
     brew install --cask basictex
     ```

2. **Update TeX Live Manager:**
   ```sh
   sudo tlmgr update --self
   ```

3. **Install required LaTeX packages:**
   If you encounter missing package errors during build, install them with:
   ```sh
   sudo tlmgr install enumitem xifthen ifmtarg xstring fontawesome6 roboto sourcesanspro tcolorbox tikzfill
   ```
   Add any other missing packages as needed.

4. **Build the document:**
   - Using VS Code with the LaTeX Workshop extension (recommended):
     - Open the `.tex` file and click "Build LaTeX project" (usually a play button in the top bar).
   - Or from the terminal:
     ```sh
     xelatex resume.tex
     ```

### Troubleshooting

- If you see errors like `! LaTeX Error: File 'packagename.sty' not found.`, install the missing package with `sudo tlmgr install packagename`.
- For persistent issues, ensure your TeX Live distribution is up to date and that your PATH includes the TeX binaries (e.g., `/Library/TeX/texbin`).

---
This project uses the [awesome-cv](https://github.com/posquit0/Awesome-CV) class.
