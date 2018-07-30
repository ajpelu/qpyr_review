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

Evolución de nombres aceptados tal y como aparecen en las distintas obras

``` r
g <- read.csv(here::here("data/names_accepted_history.csv"), header=TRUE)
kable(g)
```

|  year| litera               | genus   | specie | author | ref                          |
|-----:|:---------------------|:--------|:-------|:-------|:-----------------------------|
|  1838| Quercus toza, Bosc.  | Quercus | toza   | Bosc.  | Webb (1838)                  |
|  1854| Quercus tozza, Bosc. | Quercus | tozza  | Bosc.  | Colmeiro and Boutelou (1854) |
|  1861| Quercus tozza, Bosc. | Quercus | tozza  | Bosc.  | Amo y Mora (1861)            |
|  1861| Quercus tozza, Bosc. | Quercus | tozza  | Bosc.  | Willkomm and Lange (1861)    |
|  1870| Quercus toza, Bosc.  | Quercus | toza   | Bosc.  | Laguna y Villanueva (1870)   |

Aquí se listan las tablas de sinonimias

``` r
s <- read.csv(here::here("data/synonimia_history.csv"), header=TRUE)
kable(s)
```

| litera                           | genus   | specie      | author               | ref                       | syn | name\_acc            |
|:---------------------------------|:--------|:------------|:---------------------|:--------------------------|:----|:---------------------|
| Q. pubescens, Brot.              | Quercus | pubescens   | Brot.                | Webb (1838)               | yes | Quercus toza, Bosc.  |
| Q. humilis, D.C. non L.          | Quercus | humilis     | D.C. non L.          | Amo y Mora (1861)         | yes | Quercus tozza, Bosc. |
| Q. cerris, D.C.                  | Quercus | cerris      | D.C.                 | Amo y Mora (1861)         | yes | Quercus tozza, Bosc. |
| Q. pyrenaica, Willd.             | Quercus | pyrenaica   | Willd.               | Amo y Mora (1861)         | yes | Quercus tozza, Bosc. |
| Q. stolonifera, Lapeyr.          | Quercus | stolonifera | Lapeyr               | Amo y Mora (1861)         | yes | Quercus tozza, Bosc. |
| Q. nigra, Thore.                 | Quercus | nigra       | Thore.               | Amo y Mora (1861)         | yes | Quercus tozza, Bosc. |
| Q. tauzin, Pers.                 | Quercus | tauzin      | Pers.                | Amo y Mora (1861)         | yes | Quercus tozza, Bosc. |
| Q. brossa, Bosc.                 | Quercus | brossa      | Bosc.                | Amo y Mora (1861)         | yes | Quercus tozza, Bosc. |
| Q. aegilops, Asso.               | Quercus | aegilops    | Asso.                | Amo y Mora (1861)         | yes | Quercus tozza, Bosc. |
| Q. pubescens, Brot. non W.       | Quercus | pubescens   | Brot. non. W.        | Amo y Mora (1861)         | yes | Quercus tozza, Bosc. |
| Q. humilis, DC. non L. nec Lamk. | Quercus | humilis     | DC. non L. nec Lamk. | Willkomm and Lange (1861) | yes | Quercus tozza, Bosc. |
| Q. pyrenaica, W.                 | Quercus | pyrenaica   | W.                   | Willkomm and Lange (1861) | yes | Quercus tozza, Bosc. |
| Q. stolonifera, Lap.             | Quercus | stolonifera | Lap.                 | Willkomm and Lange (1861) | yes | Quercus tozza, Bosc. |
| Q. tauzin, P.                    | Quercus | tauzin      | P.                   | Willkomm and Lange (1861) | yes | Quercus tozza, Bosc. |
| Q. pubescens, Brot.              | Quercus | pubescens   | Brot.                | Willkomm and Lange (1861) | yes | Quercus tozza, Bosc. |
| Q. robur, Ass.                   | Quercus | robur       | Ass.                 | Willkomm and Lange (1861) | yes | Quercus tozza, Bosc. |
| Robur III, Clus.                 | Quercus |             | Clus.                | Willkomm and Lange (1861) | yes | Quercus tozza, Bosc. |

Nombres vulgares
================

Nombres vulgares recogidos en diferentes obras:

``` r
d <- read.csv(here::here("data/vulgaris_comunis.csv"), header=TRUE)

kable(d)
```

| nombre                  | sitio               | ref                          |
|:------------------------|:--------------------|:-----------------------------|
| Melojo                  | Sierra de Segura    | Colmeiro and Boutelou (1854) |
| Carvalho pardo da Beira | Portugal            | Colmeiro and Boutelou (1854) |
| Cerquiño                | Galicia             | Colmeiro and Boutelou (1854) |
| Cerqueiro               | Galicia             | Colmeiro and Boutelou (1854) |
| Roble                   | Estremadura         | Colmeiro and Boutelou (1854) |
| Roble                   | Sierra Morena       | Colmeiro and Boutelou (1854) |
| Roble                   | Granada             | Colmeiro and Boutelou (1854) |
| Roble                   | Castell. et Granat. | Willkomm and Lange (1861)    |
| Cerquiño                | Gallec.             | Willkomm and Lange (1861)    |
| Cerqueiro               | Gallec.             | Willkomm and Lange (1861)    |
| Melojo                  | Murcicis            | Willkomm and Lange (1861)    |
| Rebollo                 |                     | Laguna y Villanueva (1870)   |

-   Es común llamar *rebollo* al *Q. toza* joven y *roble* al mismo árbol ya viejo (Laguna y Villanueva 1870)

References
----------

Amo y Mora, M. del. 1861. Memoria sobre la distribucion geografica de las familias de las plantas crucíferas, leguminosas, rosáceas, salsoláceas, amentáceas, coníferas y gramíneas de la peninsula ibérica. Memorias de la Real Academia de Ciencias, Madrid:223–463.

Colmeiro, M., and E. Boutelou. 1854. Exámen de las encinas y demas árboles de la península que producen bellotas con la designacion de los que se llaman mestos. Page 16 p. Sevilla.

Laguna y Villanueva, M. 1870. Comisión de la flora forestal español. resumen de los trabajos verificados por la misma durante los años 1867 y 1868. Imprenta del Colegio Nacional de Sordo-mudos y de Ciegos. Madrid.

Webb, P. B. 1838. Iter hispaniense, or a synopsis of plants collected in the southern provinces of spain and in portugal, with geographical remarks, and observations on rare and undescribed species. Page 100. London, Béthune; Plon.

Willkomm, Moritz, and J. Lange. 1861. Prodromus florae hispanicae, seu synopsis methodica omnium plantarum in hispania. Page 358. Stuttgart,E. Schweizerbart.
