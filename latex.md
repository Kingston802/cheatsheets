# latex 
latex is a type setting system that evolved from donald knuth's 'tex' system,
it's pronounced 'lah-tek'

## compiling
the exact command depends on your system and installation but it is usually 
```bash
pdflatex filename.tex
```

## basic document structure
```latex
\documentclass[a4paper, 12pt]{article}
\begin{document}
% write here

\title{My first latex document}
\author{My Name}

\maketitle

\subheading{This is a heading}
this is regular text

\subsubheading{This is a smol heading}
this is also regular text
this is on the same line 

this is on a new line

\end{document} % make sure you include this
```
a double space will cause latex to put the sentence on a new line

## maths
latex has different 'environments' for writing maths
```latex
inline maths is written like $x=2+2$ with the dollar sign used as a delimiter

\begin{equation}
E = mc^2
\end{equation}

\begin{displaymath}
x = 1 + 2 \\
y = 2 + 3 \\
\end{displaymath}
```
\\ will break the line 
in math mode, whitespace does not matter

## important packages
if you are doing anything math related
```latex
\usepackage{amsmath, amssymbols}
```
these will give you useful symbols like 
```latex
\therefore
\implies
```
and also important display things such as align which allows you to center equations or align them with &
```latex
\begin{align*}
    x &= 3 + 5 \\
    y &= 3 + 5 \\
\end{align*}
```
if you want to include images
```latex
\usepackage{graphicx}
```
you can then use images like
```latex
\includegraphics[scale=0.5]{filename.png} % scale is optional but useful
```

if you want to use colour in any capacity
```latex
\usepackage{xcolor}
```
which gives you the commands
```latex
\color{red} % changes the colour of text after it 
\textcolor{red} % sets inline text colour
\colorbox{red} % sets background colour of text
\pagecolor{red} % sets background colour for whole page
```

## common problems 
spacing in your document
```latex
\\ % will break the line 
\* % will break the line with no indent
~ % inserts a space
```

spacing in math mode
```latex
\thinmuskip % will insert some horizontal spacing in math mode
\! % does the same as above
& % in the align environment will 'align' equations so they all line up on the &
```

double quotes 
```latex
``this is how you do proper double quotes''
```

## read more 
```bash
man latex
```
[math symbols](https://en.wikipedia.org/wiki/Wikipedia:LaTeX_symbols)

[overleaf tutorial](https://www.overleaf.com/learn/latex/Tutorials)
