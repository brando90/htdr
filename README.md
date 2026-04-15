# HTDR: How To Do Research

**De-risking Frontier Projects: A Systematic Framework & Review for Tackling High-Uncertainty Work**

A NeurIPS position paper that formalises the **Velocity--Vectoring** decision loop from Stanford CS197 into a systematic, citable framework for de-risking high-uncertainty research and engineering projects.

## Authors

Alycia Lee\*, Brando Miranda\*, Sudharsan Sundar, Sanmi Koyejo  
Stanford University  
\*Equal contribution

## Overview

The prevailing belief in CS training holds that research mastery emerges primarily through prolonged apprenticeship. We challenge this assumption by formalising Velocity--Vectoring: a decision loop that ranks uncertainties by potential impact and resolves the highest-risk item through the leanest viable experiment. The paper consolidates insights from:

- **CS197 lectures** (Michael Bernstein) -- Vectoring, Velocity, Bit Flips, Evaluations
- **ML practitioner advice** -- production hygiene, frontier-scale heuristics (Rylan Shaeffer)
- **Engineering efficiency** -- Mo Tiwani's time-management and strategic work tips
- **Writing craft** -- Larry McEnerney, Simon Peyton Jones
- **Startup methodology** -- YC founders (Stanley Tang, Walker Williams), Musk's five-step protocol
- **Career strategy** -- PhD navigation, academic positioning, tacit knowledge transmission
- **Cognitive science** -- training stable attention, psychological profiles of breakthrough innovators

## Repository Structure

```
htdr/
├── latex_paper/              # NeurIPS position paper
│   ├── 00_main.tex           # Main document (compile this)
│   ├── 01_introduction.tex   # Introduction & contributions
│   ├── 02_abstract_blueprint.tex
│   ├── 03_ml_research_advice.tex
│   ├── ...                   # One .tex file per section
│   ├── references.bib        # Bibliography
│   ├── neurips_2025.sty      # NeurIPS style
│   └── neurips.bst           # Bibliography style
├── experiments/
│   └── 00_cs197_all_notes/   # CS197 lecture transcript notes
├── CLAUDE.md                 # Agent instructions
├── agents.md                 # Cross-agent instructions
└── README.md
```

## Building the Paper

```bash
cd latex_paper
pdflatex 00_main.tex
bibtex 00_main
pdflatex 00_main.tex
pdflatex 00_main.tex
```

Or with latexmk: `latexmk -pdf 00_main.tex`

## Overleaf

Original Overleaf project: https://www.overleaf.com/project/6859e3ae3530e5cfb6e6ccd6

## Citation

```bibtex
@inproceedings{lee2025derisking,
  title={De-risking Frontier Projects: A Systematic Framework \& Review for Tackling High-Uncertainty Work},
  author={Lee, Alycia and Miranda, Brando and Sundar, Sudharsan and Koyejo, Sanmi},
  booktitle={NeurIPS 2025 Position Paper Track},
  year={2025}
}
```

## License

See [LICENSE](LICENSE) for details.
