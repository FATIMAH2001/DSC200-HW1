Homework \#1 – Pet Names Dataset
================
FATIMAH YOUSEF
2021-02-17

**Student ID:2201002709**

**Deadline:** 23:59 on Saturday, 13 February 2021

**Total Points:** 30

## Loading Packages

``` r
library(tidyverse)
library(openintro)
library(ggrepel)
```

\#\#Exercises

\`1.

(4 points)

522519 2.

(4 points)

variables = 7

1.  (4 points)

NA 483 Lucy 439 Charlle 387 Luna 355

\`4.

(10 points)

``` r
seattlepets %>%
group_by(species) %>%
count(animal_name, sort = TRUE) %>%
slice_max(n, n = 5) %>% arrange(species,n)
```

    ## # A tibble: 53 x 3
    ## # Groups:   species [4]
    ##    species animal_name     n
    ##    <chr>   <chr>       <int>
    ##  1 Cat     Max            83
    ##  2 Cat     Lily           86
    ##  3 Cat     Lucy          102
    ##  4 Cat     Luna          111
    ##  5 Cat     <NA>          406
    ##  6 Dog     Daisy         221
    ##  7 Dog     Luna          244
    ##  8 Dog     Bella         249
    ##  9 Dog     Charlie       306
    ## 10 Dog     Lucy          337
    ## # … with 43 more rows

\`5. What names are more common for cats than dogs? The ones above the
line or the ones below the line?

Oliver and Lily

(4 points)

\`6. Is the relationship between the two variables (proportion of cats
with a given name and proportion of dogs with a given name) positive or
negative? What does this mean in context of the data?

Answer here

(4 points)
