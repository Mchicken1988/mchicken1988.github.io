---
knit: "(function(inputFile, encoding) { rmarkdown::render(inputFile,
  encoding = encoding, output_dir =
  “/Users/mariokeller/privat/mchicken1988.github.io/\\_posts”,
  output_file = sub(“Rmd”, “markdown”, inputFile \\|\\>
  Biostrings::reverse() \\|\\> strsplit(“/”) \\|\\> sapply(“\\[\\[”,1) \\|\\>
  Biostrings::reverse())) })"
layout: post
output:
  md_document:
    preserve_yaml: true
    variant: markdown_github
title: Test tutorial
---

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

``` r
print(inputFile)
```

    ## [1] "/Users/mariokeller/privat/mchicken1988.github.io/tutorials_Rmds/2023-01-07-test_tutorial.Rmd"

``` r
library(ggplot2)
ggplot(mpg, aes(displ, hwy)) +
  geom_point(aes(color = class)) +
  geom_smooth(se = FALSE, method = "loess") +
  labs(
    title = "Fuel efficiency generally decreases with engine size",
    subtitle = "Two seaters (sports cars) are an exception because of their light weight",
    caption = "Data from fueleconomy.gov"
  )
```

    ## `geom_smooth()` using formula 'y ~ x'

![](/tutorials_figures/2023-01-07-test_tutorial.Rmd/unnamed-chunk-3-1.png)

# Session Information

``` r
sessionInfo()
```

    ## R version 4.1.0 (2021-05-18)
    ## Platform: x86_64-apple-darwin17.0 (64-bit)
    ## Running under: macOS Big Sur 10.16
    ## 
    ## Matrix products: default
    ## BLAS:   /Library/Frameworks/R.framework/Versions/4.1/Resources/lib/libRblas.dylib
    ## LAPACK: /Library/Frameworks/R.framework/Versions/4.1/Resources/lib/libRlapack.dylib
    ## 
    ## locale:
    ## [1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8
    ## 
    ## attached base packages:
    ## [1] stats     graphics  grDevices utils     datasets  methods   base     
    ## 
    ## other attached packages:
    ## [1] ggplot2_3.3.5
    ## 
    ## loaded via a namespace (and not attached):
    ##  [1] tidyselect_1.1.1       xfun_0.26              purrr_0.3.4           
    ##  [4] splines_4.1.0          lattice_0.20-45        colorspace_2.0-2      
    ##  [7] vctrs_0.4.1            generics_0.1.0         htmltools_0.5.2       
    ## [10] stats4_4.1.0           yaml_2.2.1             mgcv_1.8-37           
    ## [13] utf8_1.2.2             rlang_1.0.4            pillar_1.8.0          
    ## [16] glue_1.6.2             withr_2.4.2            DBI_1.1.1             
    ## [19] BiocGenerics_0.39.2    GenomeInfoDbData_1.2.7 lifecycle_1.0.1       
    ## [22] stringr_1.4.0          zlibbioc_1.39.0        Biostrings_2.61.2     
    ## [25] munsell_0.5.0          gtable_0.3.0           evaluate_0.14         
    ## [28] labeling_0.4.2         knitr_1.36             IRanges_2.27.2        
    ## [31] fastmap_1.1.0          GenomeInfoDb_1.29.8    fansi_0.5.0           
    ## [34] highr_0.9              scales_1.1.1           S4Vectors_0.31.4      
    ## [37] XVector_0.33.0         farver_2.1.0           digest_0.6.28         
    ## [40] stringi_1.7.4          dplyr_1.0.9            grid_4.1.0            
    ## [43] cli_3.3.0              tools_4.1.0            bitops_1.0-7          
    ## [46] magrittr_2.0.1         RCurl_1.98-1.5         tibble_3.1.8          
    ## [49] crayon_1.5.1           pkgconfig_2.0.3        Matrix_1.3-4          
    ## [52] assertthat_0.2.1       rmarkdown_2.11         rstudioapi_0.13       
    ## [55] R6_2.5.1               nlme_3.1-153           compiler_4.1.0
