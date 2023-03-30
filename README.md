# Journal Article Template in Markdown

[![Build and Publish](https://github.com/cpmpercussion/chroma-template/actions/workflows/main.yml/badge.svg)](https://github.com/cpmpercussion/chroma-template/actions/workflows/main.yml)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)

This is a journal article template for authoring articles with [Markdown](https://en.wikipedia.org/wiki/Markdown). Have a look at the [HTML](https://cpmpercussion.github.io/chroma-template/) and [PDF](https://cpmpercussion.github.io/chroma-template/article.pdf) output.

Although specifically designed for [Chroma: Journal of the Australasian Music Association](https://computermusic.org.au/journal/), it is licensd under [Creative Commons Zero v1.0 Universal](http://creativecommons.org/publicdomain/zero/1.0/) and free to use for any other purpose and may be modified to suit your needs.

The template, `article.md`, doubles as instructions for using Markdown for authoring an academic article. You can find a short usage guide below. By default, this template looks for a BibTeX database of references in `references.bib`.

The motivation for this project is to provide a way to author academic articles in Markdown format which can be automatically translated into an attractive 1-column PDF (generated by LaTeX), an HTML file for online display, or a Word `docx` file for sending to non-Markdown-savvy collaborators.

This is _not_ a workflow for generating ACM/IEEE/`docx` formatted submissions for traditional publishing workflows, but a template for use in web-first academic publishing (which is **even more exciting** if you think about it).

This repository uses a [GitHub Action](https://docs.github.com/en/actions) to automatically build the HTML and PDF versions of the template.

The HTML output can be viewed [here (link)](https://cpmpercussion.github.io/chroma-template/) and the pdf output is [here (link)](https://cpmpercussion.github.io/chroma-template/article.pdf)

![A picture of the template being edited in VSCode](media/markdown-editing.png?raw=true "Editing the article and viewing preview output.")

## How to use

You can download the [latest release](https://github.com/cpmpercussion/chroma-template/releases) and use it as a template for authoring an article on your own system.

You can use your choice of text editor to author your article. Put any images or media you use in your manuscript in the `media` folder.

The command line software for building the HTML and PDF outputs is easy to install (see below). To build your article you need to navigate to the folder where you have editing it and type:
```
make pdf
```
to build a PDF, and:
```
make html
```
to build an HTML file.

If you want to make a `docx` file (e.g., to send to a collaborator who isn't as Markdown-savvy as you), you can run `make docx`.

You can look inside the `Makefile` in this repository to see what `pandoc` command we are using to build the article.

Some other files to explore are:

- in the `templates` folder where the Pandoc templates and reference format file are stored.
- in the `extras` folder, where some extra scripts are stored, in particular `doc-to-md.sh` might help you to convert an existing `.docx` file into the Markdown format used in this template.

## Cloud-based workflow

An alternative to installing software on your computer is to fork this repository, and edit `article.md` in GitHub or a cloud-based markdown editor. The `.github/workflows/main.yml` file defines a GitHub action that automatically builds and publishes the article to GitHub Pages. 

You will need to enable [GitHub Pages](https://pages.github.com) on your forked repository and set the source to be the `gh-pages` branch.

## Required software

If you want to use this template and create HTML and PDF output on your own computer, you will need to install:

- [Pandoc](https://pandoc.org) (for all outputs)
- A [LaTeX environment](https://www.latex-project.org/get/) (for PDF output).
- GNU Make (Windows [installer](http://gnuwin32.sourceforge.net/packages/make.htm))

## Stretch Goals

- add a reasonable way to include a copyright (and default CC attribution) or citation block on the first page. (done! ✅)
- document a fully-online cloud-based editing workflow for this template
- fully explain how to install and use the required software for use on your own system
- automatic compilation of the `.tex`/`.html`/`.docx` versions of the template using a GitHub Action. (done! ✅)

## Credits and Inspirations

Developed by Charles Martin, 2021.

Assisted by these blog posts in particular among many others:

- <https://brainbaking.com/post/2021/02/writing-academic-papers-in-markdown/>
- <https://github.com/pandoc/pandoc-action-example>