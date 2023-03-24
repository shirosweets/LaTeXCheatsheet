# LaTeXCheatsheet

| Letra | LaTeX |
| --- | --- |
| $\alpha$ | \alpha |
| $\beta$ | \beta |
| $\gamma$ | \gamma |
| $\delta$ | \delta |
| $\epsilon$ | \epsilon |
| $\zeta$ | \zeta |
| $\eta$ | \eta |
| $\theta$ | \theta |
| $\iota$ | \iota |
| $\kappa$ | \kappa |
| $\lambda$ | \lambda |
| $\mu$ | \mu |
| $\nu$ | \nu |
| $\xi$ | \xi |
| $\omicron$ | \omicron |
| $\pi$ | \pi |
| $\rho$ | \rho |
| $\sigma$ | \sigma |
| $\tau$ | \tau |
| $\upsilon$ | \upsilon |
| $\phi$ | \phi |
| $\chi$ | \chi |
| $\psi$ | \psi |
| $\omega$ | \omega |

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
