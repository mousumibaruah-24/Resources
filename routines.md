* ideally one should write a wrapper for this but for now you can copy-paste these

```

* clean string
gen clean_string = dirty_string
forvalues i = 0/255 {
    if !inrange(`i', 48, 57) /// DIGITS
        & !inrange(`i', 65, 90) /// UPPER CASE LETTERS
        & !inrange(`i', 97, 122) { // LOWER CASE LETTERS
            quietly replace clean_string = subinstr(clean_string, `= `"char(`i')"' ', "", .)
    }
}

* lower case and remove leading and trailing whitespaces
ds, has(type string)
foreach var in `r(varlist)' {
    replace `var' = strtrim(stritrim(lower(`var')))
}


* append all files
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

* parallel lists
local listone "cat dog cow pig"
local listtwo "meow woof moo oinkoink"
local n : word count `listone'
forvalues i = 1/`n' {
   local a : word `i' of `listone'
   local b : word `i' of `listtwo'
   di "`a' says `b'"
}

* append sheets within a workbook
clear
tempfile building
save `building', emptyok

import excel using "$input/Conviction of Criminals.xlsx", describe
forvalues sheet=1/`=r(N_worksheet)' {  
    local sheetname=r(worksheet_`sheet')  
    import excel using "$input/Conviction of Criminals.xlsx", ///
    sheet("`sheetname'")  clear
    gen source = "`sheetname'"
    append using `building'
    save `building', replace
}
```