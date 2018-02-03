# Harvesting Friends and Followers

## Problem

You want to harvest all of the friends or followers for a particular user.

## Solution

Use `rtweet::get_followers()` or `rtweet::get_friends()`.

## Discussion

The aforementioned `rtweet` functions give us all the data we need and handle pagination and rate-limits.

Let's see who [Brooke Anderson](https://twitter.com/gbwanderson) follows and who follows her. She's an _incredibly talented_ data scientist, weather expert and educator. We'll pull her followers and friends and work with her data a bit more in future recipes.


```r
library(rtweet)
library(tidyverse)
```

```r
(brooke_followers <- rtweet::get_followers("gbwanderson"))
```

```
## # A tibble: 256 x 1
##               user_id
##                 <chr>
##  1 913819461727195138
##  2           25819761
##  3         2198622000
##  4           59655036
##  5 769616000593428480
##  6         2973406683
##  7           73603242
##  8         2790116012
##  9          392787202
## 10 920639877397364736
## # ... with 246 more rows
```

```r
(brooke_friends <- rtweet::get_friends("gbwanderson"))
```

```
## # A tibble: 103 x 2
##           user            user_id
##          <chr>              <chr>
##  1 gbwanderson         3230388598
##  2 gbwanderson 776596392559177728
##  3 gbwanderson         1715370056
##  4 gbwanderson          131498466
##  5 gbwanderson           97464922
##  6 gbwanderson          363210621
##  7 gbwanderson           17203405
##  8 gbwanderson 910392773081104384
##  9 gbwanderson           91333167
## 10 gbwanderson         1568606814
## # ... with 93 more rows
```

## See Also

- [Official Twitter API documentation](https://developer.twitter.com/en/docs/accounts-and-users/follow-search-get-users/overview) on friends and followers.
