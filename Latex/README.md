# LaTeX — Typesetting and Document Design

## Introduction

LaTeX is a document-preparation system widely used for academic, scientific, and technical material. It is particularly useful when a document contains complex mathematical notation or requires a carefully defined structure and consistent formatting.

The assignments in this directory explore several capabilities of LaTeX, beginning with mathematical expressions and progressing towards tables, illustrations, and longer report-style documents.

## Assignment Overview

### Assignment 2 — Mathematical Notation

The second assignment introduces the mathematical features of LaTeX.

The source demonstrates how to write expressions both within ordinary text and in separate displayed environments. It also covers a range of mathematical structures, including:

- Fractions, square roots, and other mathematical symbols.
- Greek characters and commonly used notation.
- Summation expressions and binomial notation.
- Derivatives, partial derivatives, and integrals.
- Equations spanning multiple lines.
- Aligned mathematical expressions.
- Matrices and different types of delimiters.

Packages such as `amsmath`, `amssymb`, and `amsfonts` provide additional mathematical commands and environments.

### Assignment 3 — Mathematical Layouts and Tabular Data

The third assignment explores more elaborate mathematical arrangements and the presentation of information in tables.

The source includes overbraces, underbraces, arrays, piecewise definitions, and matrix structures. It also introduces table formatting techniques such as:

- Combining cells across multiple rows.
- Setting column widths and alignment.
- Applying background colours to selected cells or rows.
- Using professional horizontal rules.
- Organizing tabular information with additional spacing and formatting.

The relevant packages include `multirow`, `xcolor`, `colortbl`, `array`, and `booktabs`, along with mathematical packages.

### Assignment 4 — Document Elements and Visual Formatting

The fourth assignment shifts attention towards the organization and appearance of document content.

It introduces different approaches to markup, including presentational, procedural, and descriptive markup.

The source demonstrates the use of:

- Bulleted, numbered, and description lists.
- Tables with controlled widths and placement.
- User-defined colours and coloured text.
- Figures and external image files.
- Image placement through the `figure` environment.
- Side-by-side content using `minipage` and horizontal spacing commands.

The exercise also addresses image-related operations such as cropping and rotation.

### Assignment 5 — Report Structure and Page Styling

The fifth assignment demonstrates how LaTeX can be used to prepare a longer report.

It uses the `report` document class with A4 paper and a 12-point base font. The document is organized into formal sections, including a title page, abstract, chapters, and lower-level headings.

Formatting features include:

- Adjusting page dimensions with `geometry`.
- Styling chapter and section headings.
- Applying colours and font changes to headings.
- Defining page headers and footers.
- Creating custom page styles with `fancyhdr`.

This exercise brings together document organization and visual formatting in a single report-style layout.

## Packages and Environments

The source files make use of several LaTeX packages and built-in environments.

| Package / Environment | Role |
|---|---|
| `amsmath` | Advanced mathematical expressions and alignment |
| `amssymb` and `amsfonts` | Additional mathematical symbols and fonts |
| `array` | Extended table-column formatting |
| `multirow` | Cells spanning multiple table rows |
| `booktabs` | Improved table rules |
| `xcolor` and `colortbl` | Text, row, and cell colouring |
| `graphicx` | Inserting and manipulating images |
| `geometry` | Controlling page dimensions and margins |
| `sectsty` | Customizing section heading styles |
| `fancyhdr` | Configuring headers and footers |

Other environments used across the assignments include `equation`, `align`, `cases`, `matrix`, `tabular`, `itemize`, `enumerate`, `description`, and `figure`.

## Compiling the Source

A LaTeX distribution is needed to build the documents.

For example, Assignment 2 can be compiled from its source directory using:

```bash
pdflatex Assgn2.tex
```

The same process can be applied to the remaining `.tex` files by changing the filename. Additional compilation passes or packages may be required depending on the document.

## Included Material

The directory contains the LaTeX source files for Assignments 2 through 5, together with compiled PDF files under `Assignments/Compiled PDFs`.

The `.tex` files provide the editable document definitions, while the PDFs provide the corresponding compiled outputs.

## Takeaway

The exercises demonstrate how LaTeX can handle both the content and presentation of technical documents. Mathematical notation, structured tables, illustrations, and report layouts can all be expressed through a consistent set of commands and environments.

The progression from individual equations to complete reports provides an overview of the flexibility of LaTeX for producing detailed and consistently formatted technical material.

## Source Verification

This description is based on the assignment source files. The compiled PDFs have not been visually checked as part of this review. The source should also be checked for a few compilation details, including a malformed fraction command in Assignment 2 and a repeated document-ending command in Assignment 3.

