# NWERC Problem Statement Styleguide

## Input Sections

Input Sections are in "Dutch style": an itemized list of lines, possibly
followed by some remarks. Most items
exactly follow one of the forms in this sample:

### Input

The input consists of:

- One line with an integer $n$ ($1 \le n \le 10$), the number of Blah.
- One line with two integers $n$ and $m$ ($1 \le n \le 10$, $1\le m \le 100$),
  the number of Foo and the number of Bar.
- One line with three integers $a$, $b$, and $c$ ($1 \le a, b, c \le 1000$, $a \neq b$, $b < c$),
  the number of Foo, the number of Bar, and the number of Baz.
- One line with $n$ integers $a_1, \ldots, a_n$ ($0\le a_i\le 10^9$ for each $i$),
  where $a_i$ is the value of Foo.
- $n$ lines, each with an integer $k$ ($0\leq k \leq 100$), ...
- $n$ lines, the $i$th of which contains two integers ...
- $n$ lines, each with a string $w$ ($1\leq |w|\leq 20$), ...
- $h$ lines with $w$ characters, each character being either ‘`#`’ or ‘`.`’, ...
- $h$ lines, each with $w$ strings of $k$ characters $c$ ($c \in \\{\texttt{r}, \texttt{g}, \texttt{b}\\}$), ...
- $n$ lines, each containing two numbers describing an event:
  - An integer $e$ ($1\leq e\leq 5$) the type of the event, and
  - a floating-point number $p$ ($0 < p < 1$ with at most $6$ digits after the decimal point),
    the probability of success.

An optional remark regarding additional guarantees goes here, i.e. that a graph
is connected or all input strings have length between $1$ and $20$ characters
and only consist of English lowercase letters (`a-z`).

<details><summary>LaTeX source</summary>

```latex
\begin{Input}
    The input consists of:
    \begin{itemize}
        \item One line with an integer $n$ ($1 \le n \le 10$), the number of Blah.
        \item One line with two integers $n$ and $m$ ($1 \le n \le 10$, $1\le m \le 100$),
            the number of Foo and the number of Bar.
        \item One line with three integers $a$, $b$, and $c$ ($1 \le a, b, c \le 1000$, $a \neq b$, $b < c$),
            the number of Foo, the number of Bar, and the number of Baz.
        \item One line with $n$ integers $a_1, \ldots, a_n$ ($0\le a_i\le 10^9$ for each $i$),
            where $a_i$ is the value of Foo.
        \item $n$ lines, each with an integer $k$ ($0\leq k \leq 100$), ...
        \item $n$ lines, the $i$th of which contains two integers ...
        \item $n$ lines, each with a string $w$ ($1\leq |w|\leq 20$), ...
        \item $h$ lines with $w$ characters, each character being either '\texttt{#}' or '\texttt{.}', ...
        \item $h$ lines, each with $w$ strings of $k$ characters $c$ ($c \in \{\texttt{w}, \texttt{r}, \texttt{g}, \texttt{b}\}$), ...
        \item $n$ lines, each containing two numbers describing an event:
        \begin{itemize}
            \item An integer $e$ ($1\leq e\leq 5$) the type of the event, and
            \item a floating-point number $p$ ($0 < p < 1$ with at most $6$ digits after the decimal point),
                the probability of succes.
        \end{itemize}
        \end{itemize}
    \end{itemize}
    An optional remark regarding additional guarantees goes here, i.e. that a graph
    is connected or all input strings have length between $1$ and $20$ characters
    and only consist of English lowercase letters (\texttt{a-z}).
\end{Input}
```

</details>

### Remarks

- Items end with a full stop.
- Use wording `One line with ...`.
- Use a comma between the description of what appears in input and the description of what it means.
- Do not write `single`. Just say `One line with an integer $n$`.
- Do not write `Then follow` for bullet points after the first one.
- When possible, mention all variables at the start of the sentence: `One line with two integers $n$ and $m$ (...), ...`.
- Do not reuse variable names.
- Separate multiple constraints into separate math environments: `($n \leq 100$, $m \leq 100$, $n \neq m$)`.
- If a constraint is symmetric around zero, use the absolute value: `($\left| x_i \right| \leq 100$)`.
- Use inclusive lower/upper bounds when possible: `($2 \leq n \leq 100$, $0 \leq m \leq 99\,999$, $1 \leq k < 2 \cdot 10^5$)`.
- When using indices, always quantify over them properly.
- Don't introduce indices unless you need them.
- Do not write "separated by single spaces" and similar general
  formatting rules that always apply (but if for some reason amount of
  spaces may vary, do write this).
- Use itemize even when there is only a single item.

| Don't                                                                                                         | Do                                                                                  |
| ------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `One line without a period`                                                                                   | `One line ending in a period.`                                                      |
| `A line with ...`, `One line containing ...`                                                                  | `One line with ... `                                                                |
| `One line with an integer $n$ not separated by a comma.`                                                      | `One line with an integer $n$, separated by a comma.`                               |
| `One line with a single integer $n$.`                                                                         | `One line with an integer $n$.`                                                     |
| `Then follow $n$ lines with ...`                                                                              | `$n$ lines with ...`                                                                |
| `One line with $n$ (..), the number of X, and $m$ (..), the number of Y.`                                     | `One line with two integers $n$ and $m$ (..), the number of X and the number of Y.` |
| `One line with an integer $x$ ($-100 \leq x \leq 100$)`                                                       | `One line with an integer $x$ ($\left \vert x \right \vert \leq 100$)`              |
| `$n$ lines each containing an integer $x_i$`                                                                  | `$n$ lines, the $i$th of which contains an integer $x_i$`                           |
| `One line with $n$ integers $x_i$ ($1 \le x_i \le 100$)`                                                      | `One line with $n$ integers $x_1, \ldots, x_n$ ($1 \le x_i \le 100$ for all $i$)`   |
| `$n$ lines, the $i$th of which contains an integer $x_i$ ($0 \le x_i \le 10$)` without refering to the $x_i$s | `$n$ lines, each containing an integer $x$ ($0 \le x \le 10$)`                      |

## Output Sections

- The basic phrasing is `Output the number of {ABC} such that {XYZ}.`
- Don't use funny output phrases, just plain
  `yes`/`no`/`possible`/`impossible` (and all lowercase), whichever is
  appropriate. The statement should both quote and texttt the text:
  ```
  ``\texttt{impossible}''
  ```
- Output is usually not space sensitive – don't write `Output two lines ...` or `Output two space-separated ...`,
  just write `Output two ...`
- Even when the output goes on multiple lines, just writing `Output the number of integers, followed by these integers.` is usually sufficient.
- If the problem is to find something or output impossible: ` If it is possible to {ABC}, output {XYZ}. Otherwise, output ``\texttt{impossible}''. `
- Real-valued tolerance: `Your answer should have an absolute or relative error of at most $10^{-6}$.` (with $10^{-6}$ replaced by
  whatever tolerance the problem uses).
  This sentence should form its own paragraph.
- Accepting any valid solution: `If there are multiple valid/optimal solutions, you may output any one of them.`
  This sentence should form its own paragraph.
- Imposing technical restrictions on the output not part of the
  underlying problem, for the purposes of making judging feasible:
  describe these after the general description of the output format
  (c.f. NWERC 2018 Circuit Design and NWERC 2018 Game Design).
- Do not use itemize.

## Samples

- For each problems, make friendly samples that show all cases.
- Ensure samples are as 'free' as allows:
  - When input is not guaranteed to be sorted, include non-sorted sample.
  - When input is arbitrary integers, do not only include positive integers.
  - ...
- For problems with real-valued output, do not hardcode the answer file (unless it's a round number).
  Instead, use an accepted submission that outputs the correct output with the desired number of digits to generate the answer of the sample.

## Interaction Sections

Instead of hardcoded `.in` and `.ans` for the samples,
you can create one or more `.interaction` files of the following form:

- each line preceded by `<` appears on the left (i.e. team input/validator output)
- each line preceded by `>` appears on the right (i.e. team output/validator input)

For example, a binary search sample could be this:

```
<10
>5
<larger
>7
<smaller
>6
<correct
```

The interaction section itself must consist of:

- An introductory paragraph, announcing that the problem is interactive
- A few paragraphs describing the input/output protocol
- Optionally "If there are multiple valid solutions, you may output any one of them."
- "The interactor is (not) adaptive", with an explanation of what this means
- "Make sure you flush the buffer after each write."
- "A testing tool is provided to help you develop your solution."
  - This testing tool is provided in `attachments/` and usually written in Python.
    See interactive problems from previous years for examples.
- "Using more than `$\maxq$` queries will result in a wrong answer."

<details><summary>You can use the following as a template:</summary>

```
\begin{Interaction}
    This is an interactive problem.
    Your submission will be run against an \emph{interactor},
    which reads from the standard output of your submission
    and writes to the standard input of your submission.
    This interaction needs to follow a specific protocol:

    The interactor first sends
    one line with two integers $w$ and $h$ ($1\leq w\leq \maxw$, $1\leq h\leq \maxh$),
    the width and height of ...

    Then, your program should make at most $\maxq$ queries to find the [answer].
    Each query is made by printing one line of the form ``\texttt{?~$x$~$y$}'' ($1\leq x\leq w$, $1\leq y\leq h$).
    The interactor will respond with ...,
    indicating the ...

    When you have determined the [answer] $x$,
    print one line of the form ``\texttt{!~$x$}'',
    after which the interaction will stop.
    Printing the answer does not count as a query.

    If there are multiple valid solutions, you may output any one of them.

    The interactor is not adaptive: the ... are fixed up front, and do not depend on your queries.

    Make sure you flush the buffer after each write.

    A testing tool is provided to help you develop your solution.

    Using more than $\maxq$ queries will result in a wrong answer.
\end{Interaction}
```

</details>

## General guidelines

Try to keep the Latex code as clean as possible, avoiding contorted
tweaks to get your problem to look like you want. It should be
possible to convert the problem statement to both PDF and HTML
reliably.

- We use [Oxford English](https://en.wikipedia.org/wiki/Oxford_spelling) for the statements.
  - Use Oxford commas when needed.
  - There should be no comma following "e.g." or "i.e.", e.g. like this.
    Preferably, use full phrases like "for example" or "that is"
    (which _are_ followed by a comma, for example, like this).
  - Use a small letter after a colon: like this.
  - Use en-dash when needed -- do not use the longer em dash.
  - Note the difference between "number" and "amount":
    the first is for countable things (e.g. number of times),
    while the latter is for uncountable things (e.g. amount of time).
  - Note the difference between "for each" (which stresses individual items)
    and "for every"/"for all" (which refers to the group of items collectively).
  - Prefer neutral singular pronouns ("they"/"their"/"them") when possible.
- Variable names: use lower case `$n$`, `$m$`, etc for numeric variables.
  For other types of variables, e.g. set-valued variables, upper case may be better.
- The default is to use $1$-based indexing of e.g. nodes in graphs and
  other sets of items given serial IDs, but in cases where $0$-based
  indexing becomes cleaner this may be OK (e.g. if there are lists of
  $n+1$ things, naming them $x_0$ up to $x_n$ may be preferable).
- Do not use phrases along the lines of "Can you help protagonist do
  X?" (in particular in cases when the answer is always yes for a
  sufficiently competent value of "you"). Instead use imperative
  form: "Help X with Y."
- The imperative verb "calculate" tends to be overused,
  you can switch it up with "compute", "find", or "determine".
- Avoid long lines in the Latex source. Shorter lines usually give better commit
  diffs where there are small changes. Either wrapping at 80/100 chars or at the
  end of sentences is fine.
- Use variables for the problem bounds, and name them specific to the problem:
  `\newcommand{\Amaxn}{10^9}`.
- Use "vertex" for graphs (including trees), and "node" for data structures.
- Write "connected undirected graph" instead of "undirected connected graph".

## Formatting/typesetting details

- Use exponents for values of $10^5$ and larger, e.g. `$10^6$` rather than `$1\,000\,000$`.
- For numbers of five or more digits, use `\,` (small space) to create groups of three
  digits, e.g. `$25\,000$`: $25\,000$ instead of $25000$.
  Smaller numbers (e.g. $2500$) are fine without separating space.
- Always put numbers in math mode throughout the text, e.g. $42$
  rather than 42.
- $i$th (`$i$th`), not $i$:th, $i$-th, or $i$'th.
- Do not use contractions (i.e. write "do not" instead of "don't", etc)
- Formatting quantities: `value\,\textrm{unit}` (e.g. `$3\,\textrm{cm}$`). This style is compatible with the [siunitx](https://ctan.org/pkg/siunitx) package.
- Formatting units: `\textrm{unit}` (e.g. `$\textrm{cm}$`).
- String literals are both ` ``quoted'' ` and `\texttt`:
  ```
  ``\texttt{impossible}''
  ```
  Quotes start with
  two backticks, and end with two single quotes.
  Single characters can be quoted by a single backtick/quote: $`\texttt{a}'$:
  ```
  `\texttt{a}'
  ```

## Images

We distinguish between two types of pictures used in problem
statements: illustrations and figures.

An **illustration** is a non-essential eye candy picture whose only
purpose is to make the problem statement look prettier. The template
provides a command `\illustration{width%}{image}{caption+attribution}` to
typeset illustrations. Its arguments are:

- `width%`: a number between 0 and 1, the desired width of the illustration, as fraction of the total page width.
- `image`: the image file to be included.
- `caption+attribution`: caption (optional) and attribution for the image

```
\illustration{0.3}{image.jpg}{Description of the illustration. CC BY-SA 4.0 by Person on \href{https://example.com/reference-to-image}{Pixabay}}
```

A **figure** is an essential picture explaining or clarifying some
part of the problem statement. Figures should be typeset using the
standard Latex figure environment and `\includegraphics`. A typical use
would be:

```
\begin{figure}[!h]
\centering
\includegraphics[width=0.5\textwidth]{a}
\caption{Illustration of Sample Input/Output 1, where the answer is 42.}
\label{fig:a}
\end{figure}
```

The figure can (and should!) then be referenced, e.g. by ending the input
section with:

```
See Figure~\ref{fig:a} for an example.
```

Note that inline graphics (like `tikz`) do not work well when converting the problem statement to HTML
(e.g. for [Kattis](https://open.kattis.com/search?q=nwerc)),
so if you want to generate a figure using inline commands,
please do so in a separate TeX file with a small `Makefile` and include the resulting PDF.
