+++
title = "CSSの効き方"
+++


## Font-weight

<div style="font-weight:normal;">
font-weight: normal; ふつう
</div>

<div style="font-weight:bold;">
font-weight: bold; ふとい
</div>

<div style="font-weight:200;">
font-weight: 200; ほそい
</div>

<div style="font-weight:400;">
font-weight: 400; ふつう
</div>

<div style="font-weight:600;">
font-weight: 600; ふとめ
</div>

<div style="font-weight:800;">
font-weight: 800; ふとい
</div>


## Font family

### 和文フォント

<div style="font-family: sans-serif;">
font-family: sans-serif; 総称サンセリフ, *総称サンセリフ*, **総称サンセリフ**
</div>

<div style="font-family: system-ui;">
font-family: system-ui; システム UI, *システム UI*, **システム UI**
</div>

<div style="font-family: 'Yu Gothic';">
font-family: 'Yu Gothic'; 游ゴシック, *游ゴシック*, **游ゴシック**
</div>

<div style="font-family: 'Yu Gothic Medium';">
font-family: 'Yu Gothic Medium'; 游ゴ・ミディアム, *游ゴ・ミディアム*, **游ゴ・ミディアム**
</div>

<div style="font-family: 'Noto Sans JP';">
font-family: 'Noto Sans JP'; ノー豆腐, *ノー豆腐*, **ノー豆腐**
</div>

<div style="font-family: 'BIZ UDGothic';">
font-family: 'BIZ UDGothic'; BIZ UD ゴシック, *BIZ UD ゴシック*, **BIZ UD ゴシック**
</div>

### 欧文フォント

<div style="font-family: 'Helvetica';">
font-family: 'Helvetica'; Helvetica, *Helvetica*, **Helvetica**
</div>

<div style="font-family: 'Segoe UI';">
font-family: 'Segoe UI'; Segoe UI, *Segoe UI*, **Segoe UI**
</div>

<div style="font-family: 'Arial';">
font-family: 'Arial'; Arial, *Arial*, **Arial**
</div>

<div style="font-family: 'Avenir Next LT Pro';">
font-family: 'Avenir Next LT Pro'; Avenir Next, *Avenir Next*, **Avenir Next**
</div>

## h2のなかの `code` 要素

こっちは普通の `inline code` の見た目。


## Syntax highlight

### Shell

```sh
git add .
git commit -m "Initial commit"
git push origin main

python3 sample.py --input sample.out --output sample.in
brew install python3
sudo apt update && sudo apt upgrade
pyenv --version
```

### Bash

```bash
#!/bin/bash

###### CONFIG
ACCEPTED_HOSTS="/root/.hag_accepted.conf"
BE_VERBOSE=false

if [ "$UID" -ne 0 ]
then
 echo "Superuser rights required"
 exit 2
fi

genApacheConf(){
 echo -e "# Host ${HOME_DIR}$1/$2 :"
}

echo '"quoted"' | tr -d \" > text.txt
```

### Markdown

```markdown
# hello world

you can write text [with links](http://example.com) inline or [link references][1].

* one _thing_ has *em*phasis
* two __things__ are **bold**

[1]: http://example.com

---

hello world
===========

<this_is inline="xml"></this_is>

> markdown is so cool

    so are code segments

1. one thing (yeah!)
2. two thing `i can write code`, and `more` wipee!
```

### python

```python
@requires_authorization(roles=["ADMIN"])
def somefunc(param1='', param2=0):
    r'''A docstring'''
    if param1 > param2: # interesting
        print 'Gre\'ater'
    return (param2 - param1 + 1 + 0b10l) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```

### R

```R
require(stats)

#' Compute different averages
#'
#' @param x \code{numeric} vector of sample data
#' @param type \code{character} vector of length 1 specifying the average type
#' @return \code{centre} returns the sample average according to the chosen method.
#' @examples
#' centre(rcauchy(10), "mean")
#' @export
centre <- function(x, type) {
  switch(type,
         mean = mean(x),
         median = median(x),
         trimmed = mean(x, trim = .1))
}
x <- rcauchy(10)
centre(x, "mean")

library(ggplot2)

models <- tibble::tribble(
  ~model_name,    ~ formula,
  "length-width", Sepal.Length ~ Petal.Width + Petal.Length,
  "interaction",  Sepal.Length ~ Petal.Width * Petal.Length
)

iris %>%
  nest_by(Species) %>%
  left_join(models, by = character()) %>%
  rowwise(Species, model_name) %>%
  mutate(model = list(lm(formula, data = data))) %>%
  summarise(broom::glance(model))
#> `summarise()` regrouping output by 'Species', 'model_name' (override with `.groups` argument)
#> # A tibble: 6 x 13
#> # Groups:   Species, model_name [6]
#>   Species model_name r.squared adj.r.squared sigma statistic  p.value    df
#>   <fct>   <chr>          <dbl>         <dbl> <dbl>     <dbl>    <dbl> <int>
#> 1 setosa  length-wi…     0.112        0.0739 0.339      2.96 6.18e- 2     3
#> 2 setosa  interacti…     0.133        0.0760 0.339      2.34 8.54e- 2     4
#> 3 versic… length-wi…     0.574        0.556  0.344     31.7  1.92e- 9     3
#> 4 versic… interacti…     0.577        0.549  0.347     20.9  1.11e- 8     4
#> 5 virgin… length-wi…     0.747        0.736  0.327     69.3  9.50e-15     3
#> 6 virgin… interacti…     0.757        0.741  0.323     47.8  3.54e-14     4
#> # … with 5 more variables: logLik <dbl>, AIC <dbl>, BIC <dbl>, deviance <dbl>,
#> #   df.residual <int>
```
