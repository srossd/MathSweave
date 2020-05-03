# MathSweave

MathSweave (or MathsWeave, in British English) allows Mathematica code and its output to be embedded directly into LaTeX source.

## Installation

Put `mathsweave.sty` and its dependency `mmacells.sty` where LaTeX can see them (an easy short-term solution is to put them in the same directory as your main `.tex} file). To compile your document, use

>    `pdflatex` --> `mathematica` --> `pdflatex` --> `pdflatex`

This is the same pattern as for using other external programs, e.g., `bibtex`.

More specifically, when you run `pdflatex job.tex` the first time, LaTeX will produce `job.m` (along with other dependencies). You should run `math -script job.m` before re-running `pdflatex` twice.

You will need the `CellsToTeX` package installed in Mathematica. Instructions for this are [here](https://github.com/jkuczm/MathematicaCellsToTeX).