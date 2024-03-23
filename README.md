# Sample files

This repository contains samples of Jupyter lab and R markdown files I have created along my studies. I've provided source and compiled PDFs for convenience. For each project the separate directory is used.

# Building PDF

### R markdown

The file `sample.Rmd` can be *knitted* into PDF in RStudio, all prerequisites are already present.

### Jupyter notebook

As this notebook contains Cyrillic's letters, PDF file was compiled manually for proper letters render. To create a PDF file yourself, `lualatex` is required.

Steps to reproduce:

1. Export Latex document from `sample.ipynb` with Jupyter lab. (optional)
2. In exported `sample.tex` file add the following line after documentclass tag (optional):
```latex
\usepackage{header.tex}
```
3. To compile the `.tex` file create `tmp` directory run `lualatex command`:
```bash
    $ mkdir tmp
    $ lualatex --output-directory=tmp sample.tex
```
The PDF file in `tmp` directory was generated.


## License

Distributed under MIT License, see LICENSE
