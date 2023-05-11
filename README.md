# LaTeXCheatsheet

## 

| Operador | LaTeX | Significado |
| --- | --- | --- |
| $\cdot$ | \cdot | Signo de multiplicacion |
| $\div$ | \div | |
| $\frac{a}{b}$ | \frac{a}{b} | Raíz cuadrada |
| $\sqrt{a}$ | \sqrt{a} | |
| $\sqrt[n]{a}$ | \sqrt[n]{a} | |
| $\approx$ | \approx | |
| $\arccos$ | \arccos | Arco coseno |
| $\arcsin$ | \arcsin | Arco seno |
| $\arctan$ | \arctan | Arco tangente |
| $\cos$ | \cos | Coseno |
| $\csc$ | \csc | Cosecante |
| $\cosh$ | \cosh | Coseno hiperbólico |
| $\ln$ | \ln | Logaritmo natural |
| $\log$ | \log | Logaritmo |
| $\sin$ | \sin | Seno |
| $\tan$ | \tan | Tangente |
| $\sec$ | \sec | Secante |
| $\exp$ | \exp | Exponencial |

## Tamano letra

| Ejemplo | LaTeX | Size |
| --- | --- | --- |
| $\tiny A$ | \tiny A | -4 |
| $\scriptsize A$ | \scriptsize A | -3 |
| $\footnotesize A$ | \footnotesize A | -2 |
| $\small A$ | \small A | -1 |
| $\normalsize A$ | \normalsize A | 0 |
| $\large A$ | \large A | 1 |
| $\Large A$ | \Large A | 2 |
| $\LARGE A$ | \LARGE A | 3 |
| $\huge A$ | \huge A | 4 |

## Letras griegas minúsculas
| Letra | LaTeX | Letra | LaTeX |
| --- | --- | --- | --- |
| $\alpha$ | \alpha | $\nu$ | \nu |
| $\beta$ | \beta | $\xi$ | \xi |
| $\gamma$ | \gamma | $\omicron$ | \omicron |
| $\delta$ | \delta | $\pi$ | \pi |
| $\epsilon$ | \epsilon | $\rho$ | \rho |
| $\zeta$ | \zeta | $\sigma$ | \sigma |
| $\eta$ | \eta | $\tau$ | \tau |
| $\theta$ | \theta | $\upsilon$ | \upsilon |
| $\iota$ | \iota | $\phi$ | \phi |
| $\kappa$ | \kappa | $\chi$ | \chi |
| $\lambda$ | \lambda | $\psi$ | \psi |
| $\mu$ | \mu | $\omega$ | \omega |

## Indices

| $p^3_{ij}$ | p^3_{ij}|

## Flechas

| Flecha | LaTeX | Flecha | LaTeX |
| --- | --- | --- | --- |
| $\rightarrow$ | \rightarrow | $\Rightarrow$ | \Rightarrow |
| $\leftarrow$ | \leftarrow | $\Leftarrow$ | \Leftarrow |
| $\rightharpoonup$ | \rightharpoonup | $\Leftrightarrow$ | \Leftrightarrow |
| $\leftharpoonup$ | \leftharpoonup | $\Longleftrightarrow$ | \Longleftrightarrow |

## Operadores

| Operador | LaTeX | Operador | LaTeX |
| --- | --- | --- | --- |
| $\sum$ | \sum | $\prod$ | \prod |
| $\int$ | \int | $\coprod$ | \coprod |
| $\bigcup$ | \bigcup | $\bigsqcup$ | \bigsqcup |
| $\bigcap$ | \bigcap | $$ | |

## Relaciones

| Relacion | LaTeX | Relacion | LaTeX |
| --- | --- | --- | --- |
| $\subset$ | \subset | $$ | |
| $\supset$ | \supset | $$ | |
| $\subseteq$ | \subseteq | $$ | |
| $\supseteq$ | \subseteq | $$ | |
| $$ | | $$ | |

## Lógica y teoría de conjuntos

| Cuantificador | LaTeX | Significado |
| --- | --- | --- |
| $\forall$ | \forall | Para todo |
| $\exists$ | \exists | Existe |
| $\exists!$ | \exists! | No existe |
| $\in$ | \in | Pertenece |
| $\in!$ | \in! | No pertenece |
| $\ni$ | \ni | Pertenece |

## Geometria

| Cuantificador | LaTeX | Significado |
| --- | --- | --- |
| $\perp$ | \perp | Perpendicular |
| $\not\perp$ | \not\perp | No perpendicular |
| $\parallel$ | \parallel | Paralelo |
| $\nparallel$ | \nparallel | No paralelo |
| $\angle$ | \angle | Angulo |
| $\measuredangle$ | \measuredangle | |

##

| $\Re$ | \Re |
| $\mathbb{R}$ | \mathbb{R} |
| $g \circ f$ | g \circ f |

## Operadores

| Operador | LaTeX |
| --- | --- |
| $\pm$ | \pm |
| $\mp$ | \mp |
| $>$ | > |
| $\geq$ | \geq |

##

| Operador | LaTeX |
| --- | --- |
| $\lim_{x\to\infty}$ | \lim_{x\to\infty} |




[**Aca**](https://www.overleaf.com/learn/latex/List_of_Greek_letters_and_math_symbols) hay una lista más detallada de letras griegas y símbolos matemáticos comunes

## Paquetes utiles:

```latex
\usepackage[a4paper, total={6.8in, 9.2in}]{geometry}
\usepackage{MnSymbol}
\usepackage{amsmath}
\usepackage{amsthm}
\usepackage{amsfonts}
\usepackage{afterpage}
\usepackage{stmaryrd}
\usepackage[skip=10pt plus1pt, indent=20pt,tocskip=2pt]{parskip}
\usepackage{titlesec}
\usepackage{graphicx}
\usepackage{inconsolata}
\usepackage{listings}
\usepackage[most]{tcolorbox}
```
# Cómo agregar imágenes:

Se necesita agregar el comando con el path a donde van a estar las imágenes:

`\graphicspath{ {./images/} }`

Opcionalmente se puede agregar un comando para simplificar las cosas:

`\newcommand{\addim}[1]{\includegraphics[width=\textwidth]{#1}}`

Por último,. agregar una imágen es simplemente llamar al comando con el nombre de la imagen sin la extensiń (.png, .jpg, etc)

\addim{app_1}

# Crear comandos custom


La sintaxis básica es:

`\newcommand{\ra}{$\rightarrow$}`

`\ra` va a ser el nuevo comando y lo que está en la segunda llave va a ser lo que se reemplace.

Para agregar arugmentos hay que poner la cantidad entre [] y luego usar #1, #2, ...

para la cantidad de argumentos:

`\newcommand{\bb}[1]{\textbf{#1}}`

# Crear text box

```latex
\documentclass{article}
\usepackage[]{mdframed}  % Para las cajas
\begin{document}

\begin{mdframed}
Test
\end{mdframed}

\end{document}
```

# Extensiones de vscode

Hay muchos editores online y IDEs, pero el editor y mostrador de vscode es bastante bueno al mostrar actualizaciones en tiempo real, hacer sugerencias, y hacer highlight de sintaxis. Yo instale varias extensiones para lograr esto, no sabria explicar cuales son importantes y cuales están de mas pero son:

 * LaTeX
 * LaTeX language support
 * LaTeX Workshop
 * LaTeX Formatter
 * Tex Preview

# Tablas de lineas y columnas:

```latex
\begin{center}
	\begin{tabular}{|| c | c | c ||}
		\hline
		Prefix        & Exp        & Valor             \\ [0.2ex]
		\hline\hline
		pico [p]      & $10^{-12}$ & 0.000000000001    \\
		\hline
		nano [n]      & $10^{-9}$  & 0.000000001       \\
		\hline
		micro [$\mu$] & $10^{-6}$  & 0.000001          \\
		\hline
		milli [m]     & $10^{-3}$  & 0.001             \\
		\hline
		-             & $10^{0}$   & 1                 \\
		\hline
		Kilo  [K]     & $10^{3}$   & 1,000             \\
		\hline
		Mega  [M]     & $10^{6}$   & 1,000,000         \\
		\hline
		Giga [G]      & $10^{9}$   & 1,000,000,000     \\
		\hline
		Tera  [K]     & $10^{12}$  & 1,000,000,000,000 \\
		\hline
	\end{tabular}
\end{center}
```

|| c | c | c || describe la cantidad de columnas y el tipo de separador entre ellas.

El begin y end center son opcionales pero asi la tabla no va a estar centrada en la pagina

# Listas

Entre las mas usadas, hay dos tipos de listas (estas tambien se pueden configurar muchísimo)

Listas enumeradas
Listas no numeradas (bullet-points)

Aca hay un ejemplo de cada una:

```latex
\begin{enumerate}
    \item \cd{931.500.000 ns \ra\ s}
    \item \cd{112 B \ra\ b}
    \item \cd{1 KB \ra\ Mb}
    \item \cd{900 bps \ra\ $\frac{b}{min}$ }
    \item \cd{10 GB \ra\ b}
\end{enumerate}
```

```latex
\begin{itemize}
    \item Los números de secuencia son de 4 bits (o sea van de 0 a 15)

    Se puede agregar texto intermedio que va a ser parte del item anterior

    \item El receptor tiene 4 búferes en total, todos de igual tamaño.
    \item Se usa la solución donde el emisor solicita espacio de búfer en el otro extremo.
\end{itemize}
```

# Molde de archivo de ejemplo

aca hay un template de un documento vacio con ciertas decisiones que se pueden configurar y los paquetes más usados para cosas matemáticas

```latex
\documentclass[12pt]{report}
    \title{\textbf{Titulo del archivo}}
    \author{Autor Autor}
    \date{Mar 2058}
    \renewcommand*\contentsname{Índice}

    \addtolength{\topmargin}{-1cm}
    \addtolength{\textheight}{3cm}
    \usepackage[a4paper, total={6.8in, 9.2in}]{geometry}
    \usepackage{MnSymbol}
    \usepackage{amsmath}
    \usepackage{amsthm}
    \usepackage{amsfonts}
    \usepackage{afterpage}
    \usepackage{stmaryrd}
    \usepackage[skip=10pt plus1pt, indent=20pt,tocskip=2pt]{parskip}
    \usepackage{titlesec}
    \usepackage{graphicx}
    \usepackage{inconsolata}
    \usepackage{listings}
    \usepackage[most]{tcolorbox}

    \tcbset{
        frame code={}
        center title,
        left=0pt,
        right=0pt,
        top=0pt,
        bottom=0pt,
        colback=gray!20,
        colframe=white,
        width=\dimexpr\textwidth\relax,
        enlarge left by=0mm,
        boxsep=5pt,
        arc=0pt,outer arc=0pt,
    }
	\graphicspath{ {./images/} }
	\titleformat{\chapter}[hang]{\normalfont\LARGE\bfseries}{Parte \thechapter:}{1em}{}

\begin{document}

% COMMANDS
\newcommand{\addim}[1]{\includegraphics[width=\textwidth]{#1}}
\newcommand{\note}[1]{{\footnotesize {\textbf{#1}}}}
\newcommand{\hnote}[1]{\note{#1}\hfill\break}
\newcommand{\scrib}[1]{\begin{color}{gray}#1\end{color}}
\newcommand{\noti}[1]{#1}
\newcommand{\bb}[1]{\textbf{#1}}
\newcommand{\ii}[1]{\textit{#1}}
\newcommand{\cd}[1]{\texttt{#1}}
\newcommand{\ra}{$\rightarrow$}
\newcommand\tab[1][0.4cm]{\hspace*{#1}}

\newcommand{\spl}{\gamma}

\newcommand{\nl}{\vspace{5mm}}
\newcommand{\ql}{\vspace{1mm}}
\newcommand{\tq}{\ |\ }

\newcommand{\mathbigO}{\mathcal{O}}
\newcommand{\mathsmallO}{
  \mathchoice
    {{\scriptstyle\mathcal{O}}}% \displaystyle
    {{\scriptstyle\mathcal{O}}}% \textstyle
    {{\scriptscriptstyle\mathcal{O}}}% \scriptstyle
    {\scalebox{.7}{$\scriptscriptstyle\mathcal{O}$}}%\scriptscriptstyle
  }

\newcommand{\diss}{\textdaggerdbl}
\newcommand{\parc}{\textdaggerdbl\textdaggerdbl}
\newcommand{\final}{$\bigstar$}

\newcommand{\Chi}{\ii{X}}
\newcommand{\Chig}{$\Chi(G)$}

\newcommand{\steo}{$\ \mathbb{T}$}

\newcommand{\splbox}[1]{
    \begin{center}
        \framebox[0.9\linewidth]{
            \begin{minipage}{0.85\linewidth}\ql#1\ql\end{minipage}
        }\par
    \end{center}
}


\newcommand{\greybox}[3]{
    \begin{center}
        \begin{tcolorbox}[skin=widget,
            boxrule=1pt,
            coltitle=black,
            colframe=black!80!white,
            colback=gray!20!white,
            width= (.9\linewidth)
        ]
            \tab\ii{#1:} \bb{#2}\ql\hfill

            #3
        \end{tcolorbox}
    \end{center}
}

\newcommand{\definition}[2]{\greybox{Def}{#1}{#2}}
\newcommand{\theorem}[2]{\greybox{Teo}{#1}{#2}}


\maketitle
\tableofcontents
\newpage

\chapter{Capitulo 1}

\section{Seccion}

\section{Sub seccion}

aca va el texto...

\end{document}
```

<!-- | $$ | | $$ | |
| $$ | | $$ | |
| $$ | | $$ | |
| $$ | | $$ | |
| $$ | | $$ | | -->

# Como hacer graficos

Dependencia al principio del archivo:

```latex
\usepackage{tikz}
```

```latex
\begin{center}
\begin{tikzpicture}[node distance={25mm}, main/.style = {draw, circle}]
    \node[main] (1) {$\source$};
    \node[main] (2) [right of=1] {A};
    \node[main] (3) [above right of=2] {B};
    \node[main] (4) [below right of=2] {C};
    \node[main] (5) [below right of=3] {D};
    \node[main] (6) [right of=5] {$t$};
    \draw[->] (1) -- node[midway, above, sloped, pos=0.5] {\small{C=30}} (2);
    \draw[->] (2) -- node[midway, above, sloped, pos=0.5] {\small{C=10}} (3);
    \draw[->] (2) -- node[midway, above, sloped, pos=0.5] {\small{C=10}} (4);
    \draw[->] (3) -- node[midway, above, sloped, pos=0.5] {\small{C=10}} (5);
    \draw[->] (4) -- node[midway, above, sloped, pos=0.5] {\small{C=10}} (5);
    \draw[->] (5) -- node[midway, above, sloped, pos=0.5] {\small{C=15}} (6);
\end{tikzpicture}
\end{center}
```

Un ej mas simple:

```latex
\begin{center}
\begin{tikzpicture}[node distance={15mm}, main/.style = {draw, circle}]
    \node[main] (1) {$x_1$};
    \node[main] (2) [above right of=1] {$x_2$};
    \node[main] (3) [below right of=1] {$x_3$};
    \node[main] (4) [above right of=3] {$x_4$};
    \node[main] (5) [above right of=4] {$x_5$};
    \node[main] (6) [below right of=4] {$x_6$};
    \draw (2) -- (4);
    \draw[->] (1) -- (2);
\end{tikzpicture}
\end{center}
```

Un ejemplo con lados curvos:

```latex
\begin{tikzpicture}[node distance={15mm}, thick, main/.style = {draw, circle}]
    \node[main] (1) {$x_1$};
    \node[main] (2) [above right of=1] {$x_2$};
    \node[main] (3) [below right of=1] {$x_3$};
    \node[main] (4) [above right of=3] {$x_4$};
    \node[main] (5) [above right of=4] {$x_5$};
    \node[main] (6) [below right of=4] {$x_6$};
    \draw[->] (1) -- (2);
    \draw[->] (1) -- (3);
    \draw (1) to [out=135,in=90,looseness=1.5] (5);
    \draw (1) to [out=180,in=270,looseness=5] (1);
    \draw (2) -- (4);
    \draw (3) -- (4);
    \draw (5) -- (4);
    \draw[->] (5) to [out=315, in=315, looseness=2.5] (3);
    \draw[->] (6) -- node[midway, above right, sloped, pos=1] {+1} (4);
\end{tikzpicture}
```

- Referencia: [Baeldung](https://www.baeldung.com/cs/latex-drawing-graphs)

