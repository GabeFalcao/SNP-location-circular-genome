---
title: "Circular Genome View"
author: "Gabriel Falcao Alencar"
date: "February, 2018"
output: 
  html_document: 
    keep_md: yes
---



Load the necessary packages

```r
library(circlize)
```

```
## ========================================
## circlize version 0.4.3
## CRAN page: https://cran.r-project.org/package=circlize
## Github page: https://github.com/jokergoo/circlize
## Documentation: http://jokergoo.github.io/circlize_book/book/
## 
## If you use it in published research, please cite:
## Gu, Z. circlize implements and enhances circular visualization 
##   in R. Bioinformatics 2014.
## ========================================
```

Next step, we will generate a plain graph to see what we need to alter.


```r
circos.initializeWithIdeogram()
text(0, 0, "default", cex = 1)
```

![](create-circular-genomes_files/figure-html/first-1.png)<!-- -->

```r
circos.info()
```

```
## All your sectors:
##  [1] "chr1"  "chr2"  "chr3"  "chr4"  "chr5"  "chr6"  "chr7"  "chr8" 
##  [9] "chr9"  "chr10" "chr11" "chr12" "chr13" "chr14" "chr15" "chr16"
## [17] "chr17" "chr18" "chr19" "chr20" "chr21" "chr22" "chrX"  "chrY" 
## 
## All your tracks:
## [1] 1 2
## 
## Your current sector.index is chrY
## Your current track.index is 2
```

```r
circos.clear()
```

Things that I want to change:  
* Space between the chromosomes;  
* Start on chromosome 1;  
* Add points to correct places;  
* #Any other alterations will be added here with info  

Start altering the location and space


```r
circos.par("start.degree" = 90)
circos.par("gap.degree" = rep(c(2, 4), 12))
circos.initializeWithIdeogram()
```

![](create-circular-genomes_files/figure-html/local-space-1.png)<!-- -->

```r
circos.clear()
```





