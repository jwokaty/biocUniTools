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
#>    Package Type  Title Description `Authors@R` VignetteBuilder biocViews Version
#>    <chr>   <chr> <chr> <chr>       <chr>       <chr>           <chr>     <chr>  
#>  1 ABSSeq  Pack… "ABS… "Inferring… NA          NA              Differen… 1.65.0 
#>  2 ABSSeq  Pack… "ABS… "Inferring… NA          NA              Differen… 1.65.0 
#>  3 ABSSeq  Pack… "ABS… "Inferring… NA          NA              Differen… 1.65.0 
#>  4 ABSSeq  Pack… "ABS… "Inferring… NA          NA              Differen… 1.65.0 
#>  5 ABSSeq  Pack… "ABS… "Inferring… NA          NA              Differen… 1.65.0 
#>  6 ABarray NA    "Mic… "Automated… NA          NA              Microarr… 1.79.0 
#>  7 ABarray NA    "Mic… "Automated… NA          NA              Microarr… 1.79.0 
#>  8 ABarray NA    "Mic… "Automated… NA          NA              Microarr… 1.79.0 
#>  9 ABarray NA    "Mic… "Automated… NA          NA              Microarr… 1.79.0 
#> 10 ABarray NA    "Mic… "Automated… NA          NA              Microarr… 1.79.0 
#> # ℹ 12,720 more rows
#> # ℹ 244 more variables: License <chr>, Encoding <chr>,
#> #   SystemRequirements <chr>, URL <chr>, BugReports <chr>, Repository <chr>,
#> #   `Date/Publication` <chr>, RemoteUrl <chr>, RemoteRef <chr>,
#> #   RemoteSha <chr>, NeedsCompilation <chr>, Author <chr>, Maintainer <chr>,
#> #   MD5sum <chr>, `_user` <chr>, `_type` <chr>, `_file` <chr>, `_fileid` <chr>,
#> #   `_filesize` <int>, `_sha256` <chr>, `_created` <chr>, `_published` <chr>, …
```
