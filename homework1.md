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

Positive , if dogs name increase the cats names increase also and also
if dogs name Decrease the cats name Decrease also in the same name of
them.

(4 points) &gt; library(tidyverse) &gt; library(openintro) &gt;
library(ggrepel) &gt; seattlepets %&gt;% + count(animal\_name, sort =
TRUE) \# A tibble: 13,930 x 2 animal\_name n <chr> <int> 1 NA 483 2 Lucy
439 3 Charlie 387 4 Luna 355 5 Bella 331 6 Max 270 7 Daisy 261 8 Molly
240 9 Jack 232 10 Lily 232 \# … with 13,920 more rows &gt; seattlepets
%&gt;% + group\_by(species) %&gt;% + count(animal\_name, sort = TRUE) \#
A tibble: 16,823 x 3 \# Groups: species \[4\] species animal\_name n
<chr> <chr> <int> 1 Cat NA 406 2 Dog Lucy 337 3 Dog Charlie 306 4 Dog
Bella 249 5 Dog Luna 244 6 Dog Daisy 221 7 Dog Cooper 189 8 Dog Lola 187
9 Dog Max 186 10 Dog Molly 186 \# … with 16,813 more rows &gt;
seattlepets %&gt;% + count(species, sort = TRUE) \# A tibble: 4 x 2
species n <chr> <int> 1 Dog 35181 2 Cat 17294 3 Goat 38 4 Pig 6 &gt;
seattlepets %&gt;% + group\_by(species) %&gt;% + count(animal\_name,
sort = TRUE) %&gt;% + slice\_max(n, n = 5) \# A tibble: 53 x 3 \#
Groups: species \[4\] species animal\_name n <chr> <chr> <int> 1 Cat NA
406 2 Cat Luna 111 3 Cat Lucy 102 4 Cat Lily 86 5 Cat Max 83 6 Dog Lucy
337 7 Dog Charlie 306 8 Dog Bella 249 9 Dog Luna 244 10 Dog Daisy 221 \#
… with 43 more rows &gt; View(seattlepets) &gt; seattlepets %&gt;% +
group\_by(species) %&gt;% + count(animal\_name, sort = TRUE) %&gt;% +
slice\_max(n, n = 5) %&gt;% arrange(species,n) \# A tibble: 53 x 3 \#
Groups: species \[4\] species animal\_name n <chr> <chr> <int> 1 Cat Max
83 2 Cat Lily 86 3 Cat Lucy 102 4 Cat Luna 111 5 Cat NA 406 6 Dog Daisy
221 7 Dog Luna 244 8 Dog Bella 249 9 Dog Charlie 306 10 Dog Lucy 337 \#
… with 43 more rows &gt; seattlepets %&gt;% + group\_by(species) %&gt;%
+ count(animal\_name, sort = TRUE) %&gt;% + slice\_max(n, n = 5) %&gt;%
arrange(species,n) &gt; seattlepets %&gt;% + group\_by(species) %&gt;% +
count(animal\_name, sort = TRUE) %&gt;% + slice\_max(n, n = 5) %&gt;%
arrange(n, species) \# A tibble: 53 x 3 \# Groups: species \[4\] species
animal\_name n <chr> <chr> <int> 1 Goat Abelard 1 2 Goat Aggie 1 3 Goat
Arya 1 4 Goat Beans 1 5 Goat Brussels Sprout 1 6 Goat Darcy 1 7 Goat
Fawn 1 8 Goat Fiona 1 9 Goat Gavin 1 10 Goat Grace 1 \# … with 43 more
rows
