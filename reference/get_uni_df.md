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
#> # A tibble: 24,339 × 253
#>    Package Title        Version `Authors@R` Description License URL   BugReports
#>    <chr>   <chr>        <chr>   <chr>       <chr>       <chr>   <chr> <chr>     
#>  1 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#>  2 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#>  3 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#>  4 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#>  5 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#>  6 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#>  7 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#>  8 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#>  9 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#> 10 Rarr    Read Zarr F… 1.11.38 "c(\nperso… "The Zarr … MIT + … "htt… https://g…
#> # ℹ 24,329 more rows
#> # ℹ 245 more variables: VignetteBuilder <chr>, biocViews <chr>, Encoding <chr>,
#> #   Roxygen <chr>, RoxygenNote <chr>, SystemRequirements <chr>,
#> #   `Config/testthat/edition` <chr>, `Config/pak/sysreqs` <chr>,
#> #   Repository <chr>, `Date/Publication` <chr>, RemoteUrl <chr>,
#> #   RemoteRef <chr>, RemoteSha <chr>, NeedsCompilation <chr>, Author <chr>,
#> #   Maintainer <chr>, MD5sum <chr>, `_user` <chr>, `_type` <chr>, …
```
