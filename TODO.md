- [X] pre- and post bullet list vertical space.
- [X] 'you've' (spacing) (see DEDICATION)
- [X] pre- and post bullet list vertical space.
- [X] Copyright/Draft As Of On all pages
- [X] mulex macro and formatting
- [X] Ensure Chapter Sections in TOC
- [X] xeCJK warnings
- [X] hbox warnings , main, Ch 01
- [ ] Ch 2 Images
- [ ] Chapter 2
- [ ] Ch2 GCA Example
- [ ] Better Dedication, Acks
- [X] Recheck TOC, LOT, LOF
- [ ] Marianne, Debby. Mike, Nancy, Allison, Jim, Dad, Kathy
- [ ] HKPolyU, Syd, Celine
- [ ] Vita to backmatter directory
- [ ] forward reference from the chordset section to the specific subsection introducing the chordset hardware
      (e.g., Section~\ref{sec:chordsets-hardware}) once that label exists
- [ ] Git LFS for large images?
# GEGLIM TODO
- [ ] Review whether \setlength{\headheight}{24pt} and \setlength{\footheight}{24pt} are necessary once the final header/footer layout is stable.
      They’re often used to suppress warnings, but the “right” values depend on font size and footer content.
- [ ] Curate the List of Symbols: scan the dissertation for additional real symbol candidates and decide which ones belong in the LOS.
- [ ] Verify whether the LOS is printing the intended glossary type.
      You’ve created symbols via \newglossary*{symbols}{...};
      the printing macro in front matter must explicitly print the symbols glossary (not the default).
      If LOS is “not printing symbols,” this mismatch is a common cause.
- [ ] If you’re using TeXstudio and want the cleanest compile loop, its docs show how to set up latexmk and forward/inverse search workflows.

## Front Matter Pages (In Order)
- [X] Committee and University Representative Page
- [X] Title Page
- [X] Copyright Page (optional)
- [X] Abstract Page(s)
- [X] Dedication Page (optional)
- [X] Acknowledgements Page (optional)
- [X] Table of Contents
- [X] List of Tables (if applicable)
- [X] List of Figures (if applicable)
- [X] List of Abbreviations (if applicable)
- [X] List of Symbols (if applicable)

## New Material
- [ ] Devices and Gestures: Gestemes and Gestons

## Blocking: render + deploy

- [ ] **Fix GEGLIM deploy to avoid 403**: ensure the rendered book output is copied into the root website output at `_site/in_progress/geglim/` (must contain `index.html`).
- [ ] Confirm `https://danmailman.net/in_progress/geglim/` returns **200** and displays the GEGLIM book homepage (not 403).
- [ ] Confirm GEGLIM **PDF** is deployed and downloadable from the GEGLIM book output directory.
- [ ] Ensure GEGLIM book outputs include required `site_libs/` under `in_progress/geglim/` (or otherwise resolve assets correctly).

## Front matter: UTC compliance

- [ ] In tex/utc_frontmatter.tex, update the degree lines and Month/Year to match your award term.
- [ ] Update committee list/ranks as needed.
- [ ] If your committee requires an "Approved:" label at the top-left of page i, uncomment it in `utc_preliminaries.tex`.
- [ ] The committee page uses “Mathematic” exactly as in your screenshot; you may want to change it to “Mathematics” if that is the official title.
- [ ] Expunge Old \UTC@FrontHeading
## Global mechanical cleanup

- [ ] **Triplet style**: Replace paired-backslash glosses `\gloss\` with single-quoted glosses `‘gloss’` (or `'gloss'` if needed), and italicize pinyin in parentheses:
- [ ] Replace stray LaTeX-like commands in prose (e.g., `\Chinese`) with plain text.

## CJK + PDF robustness

- [ ] Ensure PDF renders Hanzi correctly (no “Missing character” warnings): add CJK support (e.g., `ctex` with LuaLaTeX) in the GEGLIM book preamble.
- [ ] Confirm equations render consistently (LaTeX math) and are not dropped during conversion.

## Copyright + “as of” labeling

- [ ] Add a copyright indicator to every page (HTML + PDF).
- [ ] Add “As of <date>” to every page (prefer `date: last-modified`).
- [ ] Keep a “watching brief” for content that may impact commercialization; mark anything questionable for later review.

## Bibliography unification

- [ ] Convert EndNote exports (`.enw`) to BibTeX.
- [ ] Merge/dedupe into a single `references.bib` for the GEGLIM book.
- [ ] Normalize citation keys and ensure `csl` and `bibliography` are configured in GEGLIM `_quarto.yml`.

## Content integration workflow

- [ ] Get all info from "Optimizing_Gestural_Efficiency" directory to _dissertation
- [ ] then delete "Optimizing_Gestural_Efficiency" directory

## Future explorations

- [ ] Future Explorations: Alternative Ergonomics (Layout, KeyMapping) - Chapter on 'Gesture'
- [ ] Consider Having muLex handle the sequencing of same-prefix grids based on the number of item cells associated with "layout"
- [ ] Consider Allowing Different Layouts Currrently 8 X 4 with title and settings extra.
- [ ] Option 3 X 10 for keyboard rows with title and settings
- [ ] Consider Other KeyMapping Strategies (Alphabetic vs. Keyboard Layout (Qwerty)).

## Unsorted

- [ ] Remove any literal placeholder lines containing only `...` (invalid YAML/Markdown placeholders).
- [X] Evaluate TexWorks - It's Terrible!
- [ ] Acknowledgements: Committee, Syd Lamb, Lilly Chen, LingBaW, Celine, HKPoly Group, Huang, Craig Tanis, Two Argentinians, ChattLabs?
- [ ] Expunge \usepackage{float}
