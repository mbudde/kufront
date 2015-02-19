# KU frontpage in LaTeX

Provides a frontpage with University of Copenhagen logo following the
guidelines in the official [design guide](http://designguide.ku.dk). This
package provides a frontpage similar to the one provided by the [`ku-forside`
package](http://www.math.ku.dk/~m00cha/).

Features:

 - Contains the updated seal for the Faculty of Science from 2014.
 - Follows the guidelines for logo placement.
 - The logo grid (the figure with circles and triangles) is optional.

Todo:

 - So far only has the logo for the Faculty of Science.

## Usage

```tex
\documentclass[a4paper]{article}
\usepackage[lang=en,grid]{kufront}

\title{Some title}
\author{Some author}
\date{some. date 2015}
\project{A project}
\supervisor{Supervisor: Some supervisor}

\begin{document}
\begin{titlepage}
\maketitle
\end{titlepage}

\section{Here we go}
Bla bla bla \ldots

\end{document}
```
[Resulting PDF](https://github.com/mbudde/kufront/raw/master/example.pdf)

## Requirements

The package requires the `tikz`, `setspace`, `kvoptions` and `ifthen` packages.
If using the `memoir` document class, you need to add the command
`\DisemulatePackage{setspace}` before loading this package. The page size must
also be A4.

## Package options

<dl>
<dt><code>lang = ⟨langcode⟩</code> (default <code>da</code>)</dt>
<dd>Choose language for university name text. *langcode* can either be `en` or `da`. </dd>

<dt><code>faculty = ⟨id⟩</code> (default <code>natbio</code>)</dt>
<dd>Choose faculty. Only <code>natbio</code> is currently supported. </dd>

<dt><code>bw</code>, <code>color</code> (default <code>color</code>)</dt>
<dd>Choose between color and black/white version.</dd>

<dt><code>grid = ⟨variant⟩</code> (default off)</dt>
<dd>Enable logo grid. Variants available are: <code>light</code> (light color), <code>medium</code>, <code>dark</code> and <code>full</code> (full saturation). If no variant is given, <code>medium</code> is used.</dd>

<dt><code>usefont</code> (default <code>false</code>)</dt>
<dd>Use Adobe Garamond Pro small caps font to draw text instead of using premade PDF. Allows custom text in the header. Requires that the <code>fontspec</code> package is supported and that the font "AGaramond RegularSC" (Adobe Garamond Pro Small Caps) is available.</dd>

<dt><code>nametext</code> (default: name of faculty)</dt>
<dd>First line of text in the header. Requires <code>usefont</code> to be enabled.</dd>

<dt><code>nametextsnd</code> (default: empty)</dt>
<dd>Second line of text if in header if the text can't fit in one line. Requires <code>usefont</code> to be enabled.</dd>

<dt><code>subnametext</code> (default: name of university)</dt>
<dd>Smaller line of text in the header. Requires <code>usefont</code> to be enabled.</dd>
</dl>

## Package commands

In addition to the standard `\author`, `\title` and `\date` commands, the following are also available:
<dl>
<dt><code>\subtitle{⟨text⟩}</code></dt>
<dd>Set the subtitle.</dd>

<dt><code>\project{⟨text⟩}</code></dt>
<dd>Set the project (e.g. 'Master's Thesis').</dd>

<dt><code>\supervisor{⟨text⟩}</code></dt>
<dd>Set text describing supervisors.</dd>
</dl>
