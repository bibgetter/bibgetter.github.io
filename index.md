---
layout: default
---

# Introduction

The following is a Python script which will parse your `.aux` files looking for the auto-generated code that corresponds to a `\cite` command in your LaTeX. It will look for those keys which resemble either an arXiv identifier, or a MathSciNet identifier.

It will then use

* [`arxiv2bib`](https://github.com/nathangrigg/arxiv2bib)
* [`mr2bib`](https://github.com/bibgetter/mr2bib)

to fetch the corresponding BibTeX entries.

# Examples

There is only one way of using the script, namely by calling

    bibgetter file.aux

where `file.aux` is the auxiliary file created by LaTeX to communicate with `bibtex` or `biber`, and which will contain the information corresponding to the `\cite` commands in your LaTeX file. It is possible to pass multiple files.

The resulting BibTeX code is written to `stdout`, error messages are written to `stderr`.

# Installation

You will need to install [`arxiv2bib`](https://github.com/nathangrigg/arxiv2bib) and [`mr2bib`](https://github.com/bibgetter/mr2bib) first. For `arxiv2bib` this is [explained in their documentation](https://github.com/nathangrigg/arxiv2bib#installation).

To install `mr2bib`, clone the repository and run `python setup.py install`.

Then to install `bibgetter`, clone this repository and run `python setup.py install`.
