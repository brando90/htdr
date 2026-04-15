# Claude Code: run `git clone https://github.com/brando90/agents-config.git ~/agents-config 2>/dev/null || git -C ~/agents-config pull 2>/dev/null` to bootstrap/update config.
# Read `~/agents-config/INDEX_RULES.md` for all agent documentation and routing. Local `~/agents-config/` is the fallback if GitHub is unreachable.

## Project Overview

**htdr** (How To Do Research) is a NeurIPS position paper and research guide that formalises the Velocity-Vectoring decision loop from Stanford CS197 into a systematic framework for de-risking high-uncertainty research and engineering projects. The paper consolidates advice from CS197 lectures, ML practitioner insights, writing guides, and career strategy into a citable, actionable reference.

## Repository Structure

```
htdr/
├── latex_paper/          # NeurIPS position paper (split into per-section .tex files)
│   ├── 00_main.tex       # Main document (preamble, abstract, \input commands)
│   ├── 01_introduction.tex
│   ├── 02_abstract_blueprint.tex
│   ├── ...               # One .tex file per section
│   ├── neurips_2025.sty  # NeurIPS 2025 style file
│   ├── neurips.bst       # NeurIPS bibliography style
│   └── references.bib    # Bibliography
├── experiments/           # Experiment directories
│   └── 00_cs197_all_notes/  # CS197 lecture transcript notes
└── README.md
```

## Build Commands

```bash
# Compile the paper
cd ~/htdr/latex_paper
pdflatex 00_main.tex
bibtex 00_main
pdflatex 00_main.tex
pdflatex 00_main.tex

# Or with latexmk
latexmk -pdf 00_main.tex
```

## LaTeX Conventions

- One sentence per line in .tex source (clean diffs)
- Section files follow numbered naming: `NN_section_name.tex`
- Main file (`00_main.tex`) uses `\input{NN_section_name}` to include sections
- Author comment macros: `\todo{}`, `\andrea{}`, `\louise{}`
- Follow `~/agents-config/writing/ml_research_writing.md` when editing .tex files

## Key Entry Points

- `latex_paper/00_main.tex` — Main paper file, compile this
- `experiments/00_cs197_all_notes/` — CS197 lecture transcript notes
- `README.md` — Project overview with BibTeX citation
