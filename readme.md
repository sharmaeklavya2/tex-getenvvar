# `getenvvar`: Get environment variables in TeX

The package `getenvvar` provides the macro `\getEnvVar`.
It takes two parameters `#1` and `#2`, where
`#1` is a control sequence that will get the value of environment variable `#2`.

Example TeX code:

    \getEnvVar{\myHome}{HOME}
    My home directory is at \myHome.

In LaTeX, use `\usepackage{getenvvar}`, and in plain TeX, use `\input getenvvar.sty`.

`getenvvar` tries to use commands from package `expl3`.
If `expl3` is not available, which only happens for old TeX distributions,
`getenvvar` falls back to other methods that only work for `pdflatex`, `luatex` and `lualatex`.
