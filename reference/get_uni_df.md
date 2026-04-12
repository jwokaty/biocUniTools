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
#> # A tibble: 24,372 × 250
#>    Package Title Description biocViews URL   BugReports Version License Encoding
#>    <chr>   <chr> <chr>       <chr>     <chr> <chr>      <chr>   <chr>   <chr>   
#>  1 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#>  2 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#>  3 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#>  4 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#>  5 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#>  6 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#>  7 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#>  8 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#>  9 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#> 10 S4Vect… "Fou… "The S4Vec… Infrastr… http… https://g… 0.49.1  Artist… UTF-8   
#> # ℹ 24,362 more rows
#> # ℹ 241 more variables: `Authors@R` <chr>, VignetteBuilder <chr>,
#> #   Collate <chr>, Repository <chr>, `Date/Publication` <chr>, RemoteUrl <chr>,
#> #   RemoteRef <chr>, RemoteSha <chr>, NeedsCompilation <chr>, Author <chr>,
#> #   Maintainer <chr>, MD5sum <chr>, `_user` <chr>, `_type` <chr>,
#> #   `_file` <chr>, `_fileid` <chr>, `_filesize` <int>, `_sha256` <chr>,
#> #   `_created` <chr>, `_published` <chr>, `_jobs_job` <dbl>, …
```
