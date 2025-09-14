---
applyTo: "resume/**"
---

# Copilot Instructions for AI Agents

This repository is a LaTeX-based resume/CV project using the `awesome-cv` class. The structure and workflows are optimized for reproducible PDF builds and easy editing in VS Code.

## Project Structure
- `resume.tex`, `cv.tex`, `coverletter.tex`: Main entry points for different document types.
- `awesome-cv.cls`: Document class (not included here, see [Awesome-CV](https://github.com/posquit0/Awesome-CV)).
- Subdirectories (e.g., `cv/`): May contain modular content files (e.g., `certificates.tex`).

## Build Workflow
- **Primary build tool:** XeLaTeX (required for font and Unicode support).
- **Recommended editor:** VS Code with LaTeX Workshop extension.
- **Build command:**
  - In VS Code: Use the "Build LaTeX project" button.
  - In terminal: `xelatex resume.tex` (or `cv.tex`, etc.)
- **Package management:**
  - Use TeX Live (`tlmgr`) to install missing packages as reported by build errors.
  - Example: `sudo tlmgr install enumitem xifthen ifmtarg xstring fontawesome6 roboto sourcesanspro tcolorbox tikzfill`

## Key Conventions
- **Font and icon dependencies:** Relies on several non-default LaTeX packages (see README for full list). Always resolve missing `.sty` errors with `tlmgr`.
- **Document modularity:** Content may be split into separate `.tex` files and included via `\input{}` or `\include{}`. Maintain this modularity for clarity and reuse.
- **No custom build scripts:** All builds are standard LaTeX; no Makefiles or custom scripts are present.
- **No automated tests:** This repo is for document generation only; no code tests are present or expected.

## Troubleshooting & Patterns
- Always check the build log for missing package errors and resolve them with `tlmgr`.
- If using a minimal TeX Live install (e.g., `basictex`), expect to install many packages manually.
- For persistent build issues, verify your PATH includes `/Library/TeX/texbin`.
- The project is designed for reproducibility: all content and formatting is in version control.

## Example: Adding a New Section
- Create a new `.tex` file (e.g., `cv/certificates.tex`).
- Add `\input{cv/certificates.tex}` to your main `.tex` file at the desired location.

## References
- See `README.md` for full setup and troubleshooting details.
- See [Awesome-CV](https://github.com/posquit0/Awesome-CV) for class documentation and advanced usage.

---
_These instructions are for AI coding agents (e.g., GitHub Copilot, Copilot Chat) to maximize productivity and maintain project conventions._
