# Get jobs for an R Universe build

Adds Artifact and JobUrl

## Usage

``` r
get_jobs(uni, uni_os_branch, r_version, bioc_version)
```

## Arguments

- uni:

  character universe name

- uni_os_branch:

  character release or devel

- r_version:

  character

- bioc_version:

  character

## Value

data.frame packages in a universe

## Examples

``` r
get_jobs("bioc", "devel", "4.6.0", "3.23")
#> # A tibble: 12,730 × 252
#>    Package Title Description biocViews URL   BugReports Version License Encoding
#>    <chr>   <chr> <chr>       <chr>     <chr> <chr>      <chr>   <chr>   <chr>   
#>  1 ABSSeq  "ABS… "Inferring… Differen… NA    NA         1.65.0  GPL (>… NA      
#>  2 ABSSeq  "ABS… "Inferring… Differen… NA    NA         1.65.0  GPL (>… NA      
#>  3 ABSSeq  "ABS… "Inferring… Differen… NA    NA         1.65.0  GPL (>… NA      
#>  4 ABSSeq  "ABS… "Inferring… Differen… NA    NA         1.65.0  GPL (>… NA      
#>  5 ABSSeq  "ABS… "Inferring… Differen… NA    NA         1.65.0  GPL (>… NA      
#>  6 ABarray "Mic… "Automated… Microarr… NA    NA         1.79.0  GPL     NA      
#>  7 ABarray "Mic… "Automated… Microarr… NA    NA         1.79.0  GPL     NA      
#>  8 ABarray "Mic… "Automated… Microarr… NA    NA         1.79.0  GPL     NA      
#>  9 ABarray "Mic… "Automated… Microarr… NA    NA         1.79.0  GPL     NA      
#> 10 ABarray "Mic… "Automated… Microarr… NA    NA         1.79.0  GPL     NA      
#> # ℹ 12,720 more rows
#> # ℹ 243 more variables: `Authors@R` <chr>, VignetteBuilder <chr>,
#> #   Collate <chr>, Repository <chr>, `Date/Publication` <chr>, RemoteUrl <chr>,
#> #   RemoteRef <chr>, RemoteSha <chr>, NeedsCompilation <chr>, Author <chr>,
#> #   Maintainer <chr>, MD5sum <chr>, `_user` <chr>, `_type` <chr>,
#> #   `_file` <chr>, `_fileid` <chr>, `_filesize` <int>, `_sha256` <chr>,
#> #   `_created` <chr>, `_published` <chr>, `_jobs_job` <dbl>, …
```
