* stata code to generate .tex tables 
  - note to self: check out [`panel combine`](https://github.com/steveofconnell/PanelCombine)

```
* prelim
clear 
global estar3 star(* 0.10 ** 0.05 *** 0.01)

* define dummy data 
set obs 1000
gen xvar = runiform()
gen e = rchi2(1) - 1
gen yvar = 1 + 2*x + e 

* run regressions 
eststo est1: reg yvar xvar 
estadd ysumm
eststo est2: reg yvar xvar 
estadd ysumm
eststo est3: reg yvar xvar 
estadd ysumm
eststo est4: reg yvar xvar 
estadd ysumm

*** code for a simple table with four columns, one panel

* view as table in stata 
esttab est1 est2 est3 est4, se $estar3 keep(xvar) stats(N ymean)

* expoort to .tex file  
esttab est1 est2 est3 est4 ///
using "filename1x4.tex", fragment replace ///
mtitle("title1" "title2" "title3" "title4") ///
cells(b(fmt(3)) se(fmt(3) star par)) $estar3 ///
keep(xvar) coefl(xvar "Label") ///
booktabs nonotes collabels(none)  ///
stats(N ymean, fmt(%9.2gc) labels("N" "Mean") ///
	layout("\multicolumn{1}{c}{@}" "\multicolumn{1}{c}{@}")) 

*** code for a simple table with four columns, three panels

* first panel wouldn't have the number of obs 
esttab est1 est2 est3 est4 ///
using "filename3x4.tex", fragment replace ///
mtitle("title1" "title2" "title3" "title4") ///
cells(b(fmt(3)) se(fmt(3) star par)) $estar3 ///
keep(xvar) coefl(xvar "Label") ///
refcat(xvar "\textbf{\emph{Panel A}}", nolabel) ///
booktabs nonotes collabels(none) noobs 
* in order to add rows to a table, use the "append" option
* use nomtitle nonumber options to suppress titles 
* we dont want titles being reproduced 
esttab est1 est2 est3 est4 ///
using "filename3x4.tex", fragment append ///
cells(b(fmt(3)) se(fmt(3) star par)) $estar3 ///
keep(xvar) coefl(xvar "Label") ///
refcat(xvar "\textbf{\emph{Panel B}}", nolabel) ///
booktabs nonotes collabels(none) noobs ///
nomtitle nonumber
* the last panel should have total no of obs and other stats 
esttab est1 est2 est3 est4 ///
using "filename3x4.tex", fragment append ///
cells(b(fmt(3)) se(fmt(3) star par)) $estar3 ///
keep(xvar) coefl(xvar "Label") ///
refcat(xvar "\textbf{\emph{Panel C}}", nolabel) ///
booktabs nonotes collabels(none) nomtitle nonumber ///
stats(N ymean, fmt(%9.2gc) labels("N" "Mean") ///
    layout("\multicolumn{1}{c}{@}" "\multicolumn{1}{c}{@}")) 
```

- latex code using threeparttables

```
\usepackage{threeparttable}

\begin{table}[h!]\centering
 \begin{threeparttable} 
 \caption{Table caption goes here} \label{tab_label}
 \input{filename.tex} 
 \begin{tablenotes} \footnotesize
 \item Note: Table represents $\beta$ from <regression equation>.  * p $<$ 0.1, ** p $<$ 0.05, *** p $<$ 0.01.
 \end{tablenotes} 
 \end{threeparttable}
\end{table}
```