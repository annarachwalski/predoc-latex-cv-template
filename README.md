# predoc-latex-cv-template
 
A LaTeX CV template for predoctoral, research assistant, and graduate school
applications. Single column, two pages, with a navy accent color and a running
header on pages after the first.
 
A compiled sample is included: [`predoc-latex-cv-template.pdf`](predoc-latex-cv-template.pdf).
 
## background
 
Most CV templates target either faculty or undergrads. This one is aimed at in 
between, where an applicant has some research output (publications, manuscripts 
under review, conference presentations) but also still lists coursework, awards, 
and skills as they're not far out of undergrad. It keeps the academic sections 
that signal research experience while staying compact enough to read quickly, and 
assumes a bachelor's degree as the highest credential. If needed, it's simple to 
add a master's. 
 
## sections
 
In order: Header, Education, Research Interests, Research Experience, Policy and
Industry Experience, Peer-Reviewed Publications, Work Under Review, Conference
Presentations, Course Papers, Fellowships/Honors/Awards, Service, and Skills.
 
The sections are independent and can be reordered, renamed, or removed without
affecting the rest of the document.
 
## requirements
 
A LaTeX distribution that includes `pdflatex`: TeX Live (Linux/Windows), MacTeX
(macOS), or MiKTeX (Windows). All packages used are standard and ship with full
distributions: `geometry`, `fontenc`, `microtype`, `enumitem`, `titlesec`,
`xcolor`, `fancyhdr`, and `hyperref`. No external fonts required.
 
## usage
 
Compile from the command line:
 
```bash
pdflatex predoc-latex-cv-template.tex
```
 
Compile twice if the page 2 header does not render on the first pass, which is
expected for documents that reference page numbers.
 
The template can also be compiled on Overleaf with no local installation: create
a project and upload the `.tex` file.
 
## customization
 
- **accent color** Defined near the top as `\definecolor{navy}{HTML}{1A3E6E}`.
  Replace the hex value to change link and rule color.
- **margins** Set in `\usepackage[margin=1in]{geometry}`.
- **entries** Each position uses the `\entry` macro, which takes organization,
  location, role, and dates, followed by `\item` bullets. Use `\entrygap` between
  entries for consistent spacing.
- **citations** Publications, presentations, and papers use a plain unnumbered
  list and are formatted by hand, giving full control over citation style. This
  can be replaced with a BibTeX setup if preferred.
- **running header** The name in the top right of later pages is set in the
  `runningheader` page style.
- **adding a master's** The Education section is plain text rather than a macro,
  so a second degree can be added by duplicating the institution and degree
  lines, most recent first.
## files
 
```
predoc-latex-cv-template.tex   LaTeX source
predoc-latex-cv-template.pdf   compiled sample
README.md
LICENSE
```
 
## license
 
See LICENSE for terms.
