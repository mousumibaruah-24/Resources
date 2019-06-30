* append all files
```
clear
tempfile building
save `building', emptyok
fs
foreach f in`r(files)' {
    import excel using "`f'", clear
    gen source = "`f'"
    append using `building'
    save `building', replace
}
```

* append all sheets
```
* initialize
clear
tempfile building
save `building', emptyok

* get data
import excel using "filename.xlsx", describe

forvalues sheet=1/`=r(N_worksheet)' {  
    local sheetname=r(worksheet_`sheet')  
    import excel using "filename.xlsx", sheet("`sheetname'")  clear
    gen source = "`sheetname'"
    append using `building'
    save `building', replace
}
```

* clean string variables
```
ds, has(type string)
foreach var in `r(varlist)' {
    replace `var' = strtrim(stritrim(lower(`var')))
}
```

* parallel list
```
local listone "cat dog cow pig"
local listtwo "meow woof moo oinkoink"
local n : word count `listone'
forvalues i = 1/`n' {
   local a : word `i' of `listone'
   local b : word `i' of `listtwo'
   di "`a' says `b'"
}
```

* partialled regression
```
local yvar YVAR
local xvar XVAR
local ctrls ZVAR
local fe FEVAR
local grtype lfit
local xt "LABEL FOR X-AXIS"
local yt "LABEL FOR Y-AXIS"

cap drop ytilde_1 ytilde_1a xtilde_1 xtilde_1a
reghdfe `yvar' `ctrls', absorb(`fe') resid(ytilde_1)
sum `yvar' if e(sample) == 1
gen ytilde_1a = ytilde_1 + `r(mean)'
reghdfe `xvar' `ctrls', absorb(`fe') resid(xtilde_1)
sum `xvar' if e(sample) == 1
gen xtilde_1a = xtilde_1 + `r(mean)'

cap graph drop gr_`grtype'_`yvar'_`xvar'
tw (hist xtilde_1a, yaxis(2) fcolor(gs14) lcolor(gs14)) ///
(lfitci ytilde_1a xtilde_1a, ciplot(rline) blpattern(dash) bcolor(gs5) clcolor(black)) ///
if e(sample) == 1, legend(off) ///
xtitle("`xt'" ) ytitle("`yt'") name(gr_`grtype'_`yvar'_`xvar')

gr di  gr_`grtype'_`yvar'_`xvar'
gr export "$papfig/gr_`grtype'_`yvar'_`xvar'.eps", replace
```