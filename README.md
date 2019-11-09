# Nametag Generator

Create a PDF file with nametags using only LaTeX and a CSV list of participants.

Adapted from https://tex.stackexchange.com/a/94600 to use the `csvsimple` package.

## Requirements

* A working LaTeX [distribution](https://www.google.com/search?q=how+to+install+latex)
* The [ticket](https://ctan.org/pkg/ticket) and
  [csvsimple](https://ctan.org/pkg/csvsimple?lang=en) packages.
  Good LaTeX editors should be be able to fetch these for you from CTAN.

## Instructions

### Logo and participant data

A file called `logo.png` is used. The image is scaled to a fixed size in the
nametag template, regardless of logo resolution. One can change the template
in `nametags.tex` to work with other formats / filenames.

The CSV list `participants.csv` is expected to have columns:

`Name, AffiliationFirst, AffiliationSecond`

Change the `csvreader` command to match the CSV structure, otherwise.

### Adjustments to template

Tweak `nametags.tex`. "Ticket" refers to a nametag.
(The package was built for generating tickets, brochures, etc.)

Keep in mind that the `\put(x, y)` command considers coordinate `(0, 0)`
to be the lower-left corner.

### Generating

Either open `nametags.tex` in your LaTeX editor and create the PDF
or use the command line: `pdflatex nametags.tex`
