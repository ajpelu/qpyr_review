-   [Taxonomía](#taxonomia)
-   [Nombres vulgares](#nombres-vulgares)
    -   [References](#references)

``` r
library("here")
```

    ## here() starts at /Users/ajpelu/Dropbox/phd/phd_repos/qpyr_review

``` r
library("dplyr")
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
library("knitr")
Sys.setlocale(category = "LC_ALL", locale = "es_ES.UTF-8")
```

    ## [1] "es_ES.UTF-8/es_ES.UTF-8/es_ES.UTF-8/C/es_ES.UTF-8/C"

Taxonomía
=========

En su obra *Rariorum aliquot stirpium per Hispanias observatarum historia: libris duobus expressa* el autor francés Clusius (Charles de L'Ecluse) hace referencia al melojo como Robur II presentándo un dibujo de esta especie.

-   Respecto a la taxonomía, [Denk et al. 2017](https://doi.org/10.6084/m9.figshare.5547622.v1) proporcionan una exahustiva revisión de las diferentes clasifiaciones taxonómicas de las especies de Quercus.

Nombres vulgares
================

``` r
d <- read.csv(here::here("data/vulgaris_comunis.csv"), header=TRUE)

kable(d)
```

| nombre                  | sitio            | ref                          |
|:------------------------|:-----------------|:-----------------------------|
| Melojo                  | Sierra de Segura | Colmeiro and Boutelou (1854) |
| Carvalho pardo da Beira | Portugal         | Colmeiro and Boutelou (1854) |
| Cerquiño                | Galicia          | Colmeiro and Boutelou (1854) |
| Cerqueiro               | Galicia          | Colmeiro and Boutelou (1854) |
| Roble                   | Estremadura      | Colmeiro and Boutelou (1854) |
| Roble                   | Sierra Morena    | Colmeiro and Boutelou (1854) |
| Roble                   | Granada          | Colmeiro and Boutelou (1854) |

References
----------

Colmeiro, M., and E. Boutelou. 1854. Exámen de las encinas y demas árboles de la península que producen bellotas con la designacion de los que se llaman mestos. Page 16 p. Sevilla.
