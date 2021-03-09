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