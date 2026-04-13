# Flatten raw universe data.frame by matching R, OS, and arch information from `_jobs` with `_binaries`

Adds additional columns to `_jobs_r_xy`, `_binaries_r_xy`, `_jobs_type`,
`_jobs_arch`, `_jobs_os_`, `_binaries_os_`

## Usage

``` r
get_uni_df(raw_df)
```

## Arguments

- raw_df:

  raw data.frame from R Universe API

## Value

data.frame

## Examples

``` r
raw_df <- get_raw_uni_df("bioc")
get_uni_df(raw_df)
#> # A tibble: 24,375 × 250
#>    Package Type  Title Description `Authors@R` VignetteBuilder biocViews Version
#>    <chr>   <chr> <chr> <chr>       <chr>       <chr>           <chr>     <chr>  
#>  1 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#>  2 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#>  3 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#>  4 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#>  5 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#>  6 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#>  7 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#>  8 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#>  9 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#> 10 QUBIC   Pack… "An … "The core … "c(person(… knitr           "Statist… 1.39.2 
#> # ℹ 24,365 more rows
#> # ℹ 242 more variables: License <chr>, Encoding <chr>,
#> #   SystemRequirements <chr>, URL <chr>, BugReports <chr>, Repository <chr>,
#> #   `Date/Publication` <chr>, RemoteUrl <chr>, RemoteRef <chr>,
#> #   RemoteSha <chr>, NeedsCompilation <chr>, Author <chr>, Maintainer <chr>,
#> #   MD5sum <chr>, `_user` <chr>, `_type` <chr>, `_file` <chr>, `_fileid` <chr>,
#> #   `_filesize` <int>, `_sha256` <chr>, `_created` <chr>, `_published` <chr>, …
```
