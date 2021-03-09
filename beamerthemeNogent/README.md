# Beamer theme Nogent

Custom theme for beamer LaTeX.

In the premabule of the TeX document, put those lines

    \documentclass{beamer}
    \usetheme{Nogent}

Here is an example of a page.

![](screen-shot.png)



To change the main color of the theme (the default one is blue)

    \colorlet{beamer@blendedblue}{newcolor}

**Note :** only *normal* `block` have their color linked to this one, `alertblock` and `exampleblock` will be in red and green respectively.


## `\ajouterdansheadline`

The function `\ajouterdansheadline` allow to add some text or link in the right part of the head line (on the example above, it is a right arrow) :

    \ajouterdansheadline{\hyperlink{label}{$\rightarrow$}}

## Get the files

The two files to have in the current directory are :

* `beamerthemeNogent.sty`
* `beamercolorthemehippo.sty`

An [example](example.tex) of file is given.