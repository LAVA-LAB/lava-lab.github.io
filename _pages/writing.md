---
layout: page
permalink: /writing/
title: writing tips
description: A set of (opinionated) tips to get started with writing high-quality scientific reports.
nav: false
nav_order: 0
---


### General advice

1. Get bib entries from [dblp](https://dblp.org/rec/phd/dnb/Jansen15.html?view=bibtex&param=0) (condensed form).
2. Avoid orphans.
3. Ensure symbols are in the same line as their descriptor using `~`
	```latex
	[...] given an action~$a$ [...]
	```
4. Use vectorized figures.
5. Be consistent.
    - either British or American English
    - uniform capitalization of each heading level
6. Use `\colon` instead of `:` in function definitions, e.g.
    ```latex
    $T \colon  S \times A \rightarrow \Delta(S)$
    ```
7. Punctuate equations since they are part of the text:
    ```latex
    Mathematical expressions can be ``inline'' like this: $x^2+y^2=z^2$,
    or ``displayed'' like this:
    %
    \begin{equation*}
    x^2+y^2=z^2.
    \end{equation*}
    %
    ```
8. Use the right quotation marks.
    ```latex
    Here we see some `text in quotes'.
    ```
9. If you see an error, fix it. It is good practice to keep a file without errors or warnings, this way when you add an error it is easy to find the problem.

### Useful packages

#### Citations

The [natbib package](https://gking.harvard.edu/files/natnotes2.pdf) allow us to work with both author–year and numerical citations.

```latex
% preamble: \uspackage{natbib}

A Markov decision process \citep[MDP;][]{Puterman1994} is a tuple [...]

[...] we refer to~\citet{DBLP:journals/ai/KaelblingLC98} for more details.
```


> A Markov decision processes (MDP; Puterman 1994) is a tuple [...]  
> [...] we refer to  Kaelbling, Littman, and Cassandra (1998) for more details.



#### Automatic references

Use `cleveref` to keep references consistent.


```latex
% preamble: \usepackage{cleveref}
From \cref{eq:max}, we notice [...]
```

> From Eq. (1), we notice [...]


#### Clean tables

Get some inspiration from [clear off the table](https://www.darkhorseanalytics.com/blog/clear-off-the-table).



```latex
% Preamble: \usepackage{booktabs} \usepackage{multirow} \usepackage{xcolor}

\newcommand{\gc}[1]{\color{green!60!black}\textbf{#1}}

\begin{tabular}{@{}rrrrr@{}}
    \toprule
    \multirow{2}{*}{Algorithm} & \multicolumn{2}{c}{Reward}  & \multicolumn{2}{c}{Cost} \\ \cmidrule(lr){2-3} \cmidrule(l){4-5}
                               & Problem A      & Problem B  & Problem A   & Problem B  \\ \cmidrule(lr){2-3} \cmidrule(l){4-5}
    Method A                   & \gc{0.87}      & 0.80       & \gc{0.729}  & 0.75       \\
    Method B                   & 0.80           & \gc{0.90}  & \gc{0.847}  & 0.85       \\
\bottomrule
\end{tabular}
```

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
		{% include figure.html path="assets/img/table_example.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>        

For :snake:python/:panda_face:pandas users, consider using [pandas.DataFrame.to_latex](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_latex.html) :heart: to export your dataframe to a latex table.

### Math

#### Inline math
For inline math, that is, math inside a sentence, use `$\sum_{x \in X} x$`.

For better spacing, try to keep inline math at the same lineheight. Commands like `\frac{1}{2}` will be larger than the line and add white space above and below. Instead, use `$\nicefrac{1}{2}$`.

#### Display math

Display math can be done in several ways. For single equations, use
```latex
\[
\sum_{x \in X} x
\]

% or
\begin{equation}
\sum_{x \in X} x
\end{equation}
```
Make sure equations you want to refer to later are numbered.

Multiple lines of math, for example to write equation systems or if your equation doesn't fit a single line, can be done via the align environment:
```latex
\begin{align}
\sum_{x \in X} & = f(x) \\
	& + g(x). 
\end{align}
```

