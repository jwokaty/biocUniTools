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
#> # A tibble: 24,287 × 253
#>    Package Version Date       Title        Description Author Maintainer License
#>    <chr>   <chr>   <chr>      <chr>        <chr>       <chr>  <chr>      <chr>  
#>  1 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#>  2 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#>  3 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#>  4 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#>  5 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#>  6 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#>  7 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#>  8 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#>  9 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#> 10 edgeR   4.9.5   2026-04-08 Empirical A… "Different… "Yuns… "Yunshun … GPL (>…
#> # ℹ 24,277 more rows
#> # ℹ 245 more variables: VignetteBuilder <chr>, URL <chr>, biocViews <chr>,
#> #   NeedsCompilation <chr>, Repository <chr>, `Date/Publication` <chr>,
#> #   RemoteUrl <chr>, RemoteRef <chr>, RemoteSha <chr>, MD5sum <chr>,
#> #   `_user` <chr>, `_type` <chr>, `_file` <chr>, `_fileid` <chr>,
#> #   `_filesize` <int>, `_sha256` <chr>, `_created` <chr>, `_published` <chr>,
#> #   `_jobs_job` <dbl>, `_jobs_time` <int>, `_jobs_config` <chr>, …
```
