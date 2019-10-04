
## Creates LaTeX tables from csv files

This is a command line tool that automatically creates LaTeX tables from CSV files.

## Installation

```
$ git clone https://github.com/mkomod/csv2tex
```

## Usage

Example csv file named `input.csv`

```
one, two, three, four
1,2,3,4
5,6,7,8
```

```
$ csv2tex input.csv ouput.tex
```

Creates

```
\begin{table}[htp]
    \centering
    \begin{tabular}{ c  c  c  c }
        \hline
        one &  two &  three &  four \\ 
        \hline
        1 & 2 & 3 & 4 \\
	5 & 6 & 7 & 8 \\
        \hline
    \end{tabular}
\end{table}
```

### Boarders

Boarders can be added to the table by using the `-b` flag

```
$ csv2tex -b input.csv ouput.tex
```

### Printing to console

If the file output name is left blank then the content will print to the console

```
$ csv2tex input.csv
```






