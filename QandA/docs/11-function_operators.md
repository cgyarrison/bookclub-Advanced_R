# Function operators



## 11.1 Introduction {-}

:::question
> A function operator is a function that takes one (or more) functions as input and returns a function as output

...How exactly does this definition differ from a function factory?
:::

<!--html_preserve--><style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#uaaqfzvwxb .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#uaaqfzvwxb .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#uaaqfzvwxb .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#uaaqfzvwxb .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 4px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#uaaqfzvwxb .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#uaaqfzvwxb .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#uaaqfzvwxb .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#uaaqfzvwxb .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#uaaqfzvwxb .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#uaaqfzvwxb .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#uaaqfzvwxb .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#uaaqfzvwxb .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#uaaqfzvwxb .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#uaaqfzvwxb .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#uaaqfzvwxb .gt_from_md > :first-child {
  margin-top: 0;
}

#uaaqfzvwxb .gt_from_md > :last-child {
  margin-bottom: 0;
}

#uaaqfzvwxb .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#uaaqfzvwxb .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#uaaqfzvwxb .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#uaaqfzvwxb .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#uaaqfzvwxb .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#uaaqfzvwxb .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#uaaqfzvwxb .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#uaaqfzvwxb .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#uaaqfzvwxb .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#uaaqfzvwxb .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#uaaqfzvwxb .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#uaaqfzvwxb .gt_left {
  text-align: left;
}

#uaaqfzvwxb .gt_center {
  text-align: center;
}

#uaaqfzvwxb .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#uaaqfzvwxb .gt_font_normal {
  font-weight: normal;
}

#uaaqfzvwxb .gt_font_bold {
  font-weight: bold;
}

#uaaqfzvwxb .gt_font_italic {
  font-style: italic;
}

#uaaqfzvwxb .gt_super {
  font-size: 65%;
}

#uaaqfzvwxb .gt_footnote_marks {
  font-style: italic;
  font-size: 65%;
}
</style>
<div id="uaaqfzvwxb" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;"><table class="gt_table">
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1">Term</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1">Required Input</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1">Optional Input</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1">Output</th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr>
      <td class="gt_row gt_left">Functionals</td>
      <td class="gt_row gt_left">Function</td>
      <td class="gt_row gt_left">Vector</td>
      <td class="gt_row gt_left">Vector</td>
    </tr>
    <tr>
      <td class="gt_row gt_left">Function Factory</td>
      <td class="gt_row gt_left">NA</td>
      <td class="gt_row gt_left">Vector,Function</td>
      <td class="gt_row gt_left">Function</td>
    </tr>
    <tr>
      <td class="gt_row gt_left">Function Operator</td>
      <td class="gt_row gt_left">Function</td>
      <td class="gt_row gt_left">Function</td>
      <td class="gt_row gt_left">Function</td>
    </tr>
  </tbody>
  
  
</table></div><!--/html_preserve-->

> Function operators are closely related to function factories; indeed they’re just a function factory that takes a function as input

:::question
Can anyone confirm that, by definition, function operators can only take functions as inputs (and not any kind of vector)? Book quote: "A function operator is a function that takes one (or more) functions as input and returns a function as output." If this is true, then something like the following would only be a function factory, not both a function factory and a function operator:


```r
sleepy <- function(f, n){
  force(f)
  function(...){
    cat(
      glue::glue('Sleeping for {n} second{ifelse(n != 1, "s", "")}.'), 
      sep = '\n'
    )
    Sys.sleep(n)
    f(...)
  }
}

sleepy_print <- sleepy(print, 1.5)
sleepy_print('hello world')
```

```
## Sleeping for 1.5 seconds.
## [1] "hello world"
```
:::


Function factories are “any function that returns a function” and Hadley uses “simple” examples where you pass in a numeric or character to get back a customized function (pass a number to a power function to get a function dedicated to cubes)

Function operators are factories where you pass in a function and modify its behaviour a little, without actually building up the logic for a function from scratch. The operator does not supply the actual meat of the logic.
examples: `safely`, `silently`, `rate-limity` etc


## 11.2.1 purrr::safely {-}

:::question
It seems like safely is a condition wrapper - are all conditions a kind of function operator?
:::

`safely`/`possibly`/`quietly` are function operators that are condition-wrappers, but `tryCatch`/`withCallingHandlers` are not function operators (they catch the outputs and do X thing but don't actually return a function)

:::question
How would we apply `safely` to find which dataframe in a list of dataframes is causing an error?
:::


```r
library(tidyverse)

random_starwars <- function() { 
  starwars %>%
    sample_n(50) %>%
    select(name, height,mass)
}
	
broken_starwars <- function(){ 
  starwars %>%
  sample_n(50) %>%
  select(name, height,mass) %>% 
  mutate(height = as.character(height))
}
  
list_data <- list(a = random_starwars(),
                  b = random_starwars(),
                  c = broken_starwars(),
                  d = random_starwars())

map_dfr_safely <- function(.x, .f, ... ) {
  results <- map(.x, safely(.f), ...)
  list(result = bind_rows(!!!map(results, "result")), error = map(results, "error"))
}    

map_dfr_safely(list_data, semi_join, filter_starwars, by = c("name", "height"))
```

```
## Warning in is.data.frame(y): restarting interrupted promise evaluation

## Warning in is.data.frame(y): restarting interrupted promise evaluation

## Warning in is.data.frame(y): restarting interrupted promise evaluation
```

```
## $result
## data frame with 0 columns and 0 rows
## 
## $error
## $error$a
## <simpleError in is.data.frame(y): object 'filter_starwars' not found>
## 
## $error$b
## <simpleError in is.data.frame(y): object 'filter_starwars' not found>
## 
## $error$c
## <simpleError in is.data.frame(y): object 'filter_starwars' not found>
## 
## $error$d
## <simpleError in is.data.frame(y): object 'filter_starwars' not found>
```

## 11.2.2 memoise {-}

How do you check how much memory is allocated to memoise's caching? 


```r
random_starwars <- function(...){ 
  starwars %>%
    sample_n(3) %>%
    select(name)}
memoised_starwars <- memoise(random_starwars)
a <- random_starwars()
b <- memoised_starwars(1)
c <- memoised_starwars(2)
d <- memoised_starwars(3)

lobstr::obj_size(get("_cache",environment(memoised_starwars)))
```

```
## 16,232 B
```

:::question
Could we create a memoise wrapper that clears the cache when that's a certain number?
:::


```r
random_starwars <- function(...){ 
  dplyr::starwars %>%
    dplyr::sample_n(3) %>%
    dplyr::select(name)
  }
cache_memory_size <- function(f) {
  cache <- get("_cache", environment(f))
  lobstr::obj_size(cache)
}
capped_memoise <- function(..., .cache_size) {
  force(.cache_size)
  .self_ref <- memoise::memoise(...)
  f <- function(...) {
    env <- parent.env(environment())
    cache_size <- cache_memory_size(env[["_self_ref"]])
    if (cache_size > env[["_cache_size"]]) {
      message(paste0("Clearing cache [@",cache_size,"]\n"))
      memoise::forget(env[["_self_ref"]])
    }
    env[["_self_ref"]](...)
  }
  assign("_cache_size", .cache_size, environment(.self_ref))
  assign("_self_ref", .self_ref, environment(.self_ref))
  environment(f) <- environment(.self_ref)
  f
}
capped_memoised_starwars <- capped_memoise(random_starwars, .cache_size = 30000)
for (i in 1:100) {
  capped_memoised_starwars(i)
  print(cache_memory_size(capped_memoised_starwars))
}
```

```
## 14,472 B
## 15,392 B
## 16,280 B
## 17,176 B
## 18,080 B
## 18,920 B
## 19,760 B
## 20,672 B
## 21,576 B
## 22,408 B
## 23,240 B
## 24,080 B
## 24,920 B
## 25,816 B
## 26,592 B
## 27,488 B
## 28,264 B
## 29,032 B
## 29,864 B
## 30,776 B
```

```
## Clearing cache [@30776]
```

```
## 14,432 B
## 15,344 B
## 16,232 B
## 17,136 B
## 17,968 B
## 18,808 B
## 19,704 B
## 20,624 B
## 21,464 B
## 22,240 B
## 23,136 B
## 23,912 B
## 24,752 B
## 25,528 B
## 26,320 B
## 27,176 B
## 27,952 B
## 28,728 B
## 29,504 B
## 30,344 B
```

```
## Clearing cache [@30344]
```

```
## 14,432 B
## 15,344 B
## 16,184 B
## 17,088 B
## 17,928 B
## 18,784 B
## 19,624 B
## 20,464 B
## 21,352 B
## 22,256 B
## 23,088 B
## 23,984 B
## 24,760 B
## 25,680 B
## 26,520 B
## 27,408 B
## 28,184 B
## 29,056 B
## 29,896 B
## 30,736 B
```

```
## Clearing cache [@30736]
```

```
## 14,432 B
## 15,328 B
## 16,240 B
## 17,080 B
## 18,000 B
## 18,896 B
## 19,720 B
## 20,560 B
## 21,456 B
## 22,312 B
## 23,152 B
## 23,992 B
## 24,824 B
## 25,600 B
## 26,368 B
## 27,200 B
## 28,104 B
## 28,816 B
## 29,656 B
## 30,544 B
```

```
## Clearing cache [@30544]
```

```
## 14,424 B
## 15,320 B
## 16,232 B
## 17,152 B
## 18,048 B
## 18,920 B
## 19,752 B
## 20,584 B
## 21,424 B
## 22,136 B
## 22,976 B
## 23,752 B
## 24,584 B
## 25,424 B
## 26,200 B
## 27,040 B
## 27,952 B
## 28,792 B
## 29,632 B
## 30,536 B
```

:::question
Can we come up with simple example for these function operators?
:::


```r
x <- list(
  c(0.512, 0.165, 0.717),
  c(0.064, 0.781, 0.427),
  c(0.890, 0.785, 0.495),
  "oops"
)

f <- function(...) {sum(...)}
```

#### possibly {-}


```r
map_dbl(x, possibly(f, NA))
```

```
## [1] 1.394 1.272 2.170    NA
```

#### quietly {-}

Quetly doesn't work on errors, only warnings:


```r
map(x, quietly(function(x) tryCatch(f(x), error = function(e) warning(e)))
```

#### auto_browser {-}


```r
map_dbl(x, auto_browse(f))
```

## 11.2.3.1 Exercises {-}

:::question
> Vectorize() provides a convenient and concise notation to iterate over multiple arguments, but has some major drawbacks that mean you generally shouldn’t use it.

What are these drawbacks the solution manual is referring to?
:::


#### [Dean's Way](https://deanattali.com/blog/mutate-non-vectorized/)


```r
library(tidyverse)
patient_name <- function(path) {
  path_list <- str_split(path, "/") %>% unlist()
  paste(path_list[length(path_list) - 1], path_list[length(path_list)], sep = "_")
}

# Vectorize it with Vectorize
patient_name_v <- Vectorize(patient_name)
patient_name_v(path = c("some/path/abc/001.txt", "another/directory/xyz/002.txt"))
```

```
##         some/path/abc/001.txt another/directory/xyz/002.txt 
##                 "abc_001.txt"                 "xyz_002.txt"
```

#### [Jim's Way](https://www.jimhester.com/post/2018-04-12-vectorize/)


```r
patient_name_best <- function(path) {
  paste0(basename(dirname(path)), "_", basename(path))
}
```


1. `SIMPLIFY` logical or character string; attempt to reduce the result to a vector, matrix or higher dimensional array; see the simplify argument of sapply. **This means the type of the function output depends on the input.**


```r
patient_name_v("some/path/abc/001.txt")
```

```
## some/path/abc/001.txt 
##         "abc_001.txt"
```

```r
patient_name_v(character())
```

```
## named list()
```

```r
patient_name_v(NULL)
```

```
## list()
```

2. Vectorize does not generate functions with easily inspect-able code
3. Vectorize functions use `do.call()`, which can have unexpected performance consequences
4. Vectorize does not actually make your code execute faster

