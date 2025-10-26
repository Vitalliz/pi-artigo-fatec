---
description: Repository Information Overview
alwaysApply: true
---

# LaTeX Academic Paper Template Information

## Summary
This repository contains a LaTeX template for academic papers specifically designed for FATEC (Faculdade de Tecnologia) students. The template is structured for scientific articles with predefined sections including introduction, objectives, state of the art, methodology, and results. The current implementation focuses on a project called "NitrusLeaf" which aims to identify nutritional deficiencies in Citrus reticulata (mandarin) leaves using computer vision and artificial intelligence.

## Structure
- **Topicos/**: Contains separate TeX files for each section of the paper (introduction, objectives, methodology, etc.)
- **Illustrations/**: Contains images and figures used in the document
- **Logos/**: Contains logo images
- **Extras/**: Contains additional TeX files for post-textual elements

## Language & Runtime
**Language**: LaTeX
**Version**: LaTeX2e (2005/12/01 or newer)
**Build System**: Make (via makefile and make.bat)
**Package Manager**: TeX package system (via \usepackage)

## Dependencies
**Main Dependencies**:
- fatec-article.sty (Custom style package)
- babel (Multilingual support)
- biblatex (Bibliography management)
- graphicx (Image handling)
- hyperref (Hyperlinks and PDF metadata)
- algorithm, algpseudocode (Algorithm formatting)
- amsmath (Mathematical typesetting)
- float (Figure positioning)

## Build & Installation
The repository includes both a makefile (for Unix-like systems) and make.bat (for Windows) with the following build commands:

```bash
# Using makefile (Unix/Linux/macOS)
make pdf2       # Create PDF using pdflatex
make pdf3       # Create PDF using xelatex
make pdf4       # Create PDF using lualatex
make all2       # Create PDF using pdflatex and clean intermediate files

# Using make.bat (Windows)
make.bat pdf2   # Create PDF using pdflatex
make.bat pdf3   # Create PDF using xelatex
make.bat pdf4   # Create PDF using lualatex
make.bat all2   # Create PDF using pdflatex and clean intermediate files
```

## Document Structure
**Main File**: fatec-template.tex
**Bibliography**: fatec-article.bib
**Style Definition**: fatec-article.sty
**Content Organization**:
- Main document structure in fatec-template.tex
- Content sections separated into individual files in the Topicos/ directory
- References managed through BibLaTeX with the ABNT citation style
- Multilingual support (Brazilian Portuguese as primary, English as secondary)

## Configuration Options
The template supports various configuration options through the style package:
- Layout options (A or B)
- Font selection (Arial, Calibri, Times, or default LaTeX fonts)
- Section numbering and alignment
- Caption and source alignment
- Citation styles (Author-Year, Numeric, or Numeric Square Brackets)
- DOI and URL formatting in references

## Document Compilation
The document can be compiled using different LaTeX engines:
- pdfLaTeX (recommended for standard usage)
- XeLaTeX (for advanced font features)
- LuaLaTeX (for complex documents with Lua scripting)
- Traditional LaTeX → DVI → PS → PDF workflow

The build process includes bibliography processing with either biber (default) or bibtex, and optional index generation with makeindex.