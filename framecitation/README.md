# Frame Citation package

Add citations to the current frame, on the top right corner of the page.
In the premable of the TeX file write :

```
\usepackage[<options>]{framecitation}
\addbibresource{<bib_file.bib>}
```

Here is an [example](example.tex).

## Required Packages

- [`tikz`](https://www.ctan.org/pkg/pgf)
- [`biblatex`](https://ctan.org/pkg/biblatex)
- [`graphics`](https://www.ctan.org/pkg/graphics)


## Options available

- Set the offset in order to avoid the citation being over top bar(s), depending on the chosen theme
	- `bar` for the themes with one top bar
	- `compress` for the themes with two compressed top bars
	- You can edit the file [`framecitation.sty`](framecitation.sty) to set a personnalized size, on that model : `\DeclareOption{<persoOffset>}{\renewcommand{\yoffset}{<value>}}`, where `<persoOffset>` is the name of the option and `<value>` corresponds to the siize of the vertical offset (positive number). You can also use the macro `\setx`
- If the citation are too long and go beyond the right of the page, the options `long`, `Long`, `LONG` will decay the texts to the left. Default is `normal`.


## Macros

- `\setxnormal` / `\setxlong` / `\setxLong` / `\setxLONG` : change the left decay of citations set
- `\setxLONGEST` : decays the most possible to the left the citations
- `\setx{<long>}` : set a personalized x decay value
- `\citeonframe{bib_entry}` : add a citation


## Warnings

- If the citation are still too long, they will go beyond the right of the page, try to shorten them !
- Unless you custom the citation style, it is possible that some element don't appear on the page depending on the beamer chosen theme (for example, with the theme `Madrid` the author is written with the same color as the background of the top bar, so we can't see it !)
- In certain cases (too high horizontal value, or too many citation on a page), the citation may be above the content of the frame
