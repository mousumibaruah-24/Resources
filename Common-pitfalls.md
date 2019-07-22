* build 
  - [Not mapping the netCDF before extracting data from it](https://gis.stackexchange.com/questions/199972/values-extracted-from-netcdf-not-matching-original-raw-data) 
  - [Common Stata mistakes](https://github.com/matthieugomez/stata-pitfalls/wiki)
  - [Top ten Stata gotchas](https://www.ifs.org.uk/docs/stata_gotchasJan2014.pdf)
  - using `encode` to define unique IDs in different datasets before merging them 
  - not ensuring that unique IDs have a fixed length (pro tip: you can define new string variables which embed numeric codes with leading zeros `gen newvar = string(var1,"%02.0f") + string(var2, "%03.0f")`

* analysis
  - watch out for the N: missing values in 'control' variables i.e. other than the outcome or primary predictor could cause the estimating sample to change