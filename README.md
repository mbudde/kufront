# KU frontpage in LaTeX

Provides a frontpage with University of Copenhagen logo following the
guidelines in the official [design guide](http://designguide.ku.dk). This
package provides a frontpage similar to the one provided by the [`ku-forside`
package](http://www.math.ku.dk/~m00cha/).

The pros:

 - Contains the updated seal for the Faculty of Science from 2014.
 - Follows the guidelines for logo placement.
 - The logo grid (the figure with circles and triangles) is optional.

The cons:

 - Only provides a frontpage.
 - So far only has the logo for the Faculty of Science.

## Usage

```tex
\documentclass[a4paper]{article}
\usepackage[en,color,grid]{kufront}

\title{Some title}
\author{Some author}
\date{some. date 2015}
\project{A project}
\supervisor{Supervisor: Some supervisor}

\begin{document}
\maketitle

\section{Here we go}
Bla bla bla \ldots

\end{document}
```
[Resulting PDF](https://github.com/mbudde/kufront/raw/master/example.pdf)

Available options:

- `en`, `da`: Choose between danish and english text (default `da`).
- `color`, `bw`: Choose between color and black/white version (default `color`).
- `grid`: Enable logo grid (disabled by default).
