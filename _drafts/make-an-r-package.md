R package

Notes on making an R package from scratch

Using RStudio's R package menu drive system to initialize it.

First, create a README file

Then, Put some R code into the R file, being sure to use R2Oxygen comments `#'`

In the first line, write the name of the function, and then tell us what it does.

```
#' shadow_df
#'
#' \code{shadow_df} creates a data frame of class 'tbl_df' that 
#'
#' 
#'
```

Then, before the funciton, @export it

```
#' @export

shadow_df <- function(x){
  x %>%
    is.na.data.frame %>%
    as.data.frame %>% 
    as_data_frame
}
```

Make sure that any packages your code requires, you `@import`.

```
#' shadow_df
#'
#' \code{shadow_df} creates a data frame of class 'tbl_df' that
#'
#' @import dplyr
#' @import magrittr
#'
#' @export

shadow_df <- function(x){
  x %>%
    is.na.data.frame %>%
    as.data.frame %>%
    as_data_frame
}
```

Make sure you include the parameter

Edit your DESCRIPTION file, add the packages that your package using: `devtools::use_package("package")`

Then, use the command,

`devtools::load_all()`

Make sure there are no errors.

Then run the documentation

`devtools::document()`

Then build

Then check

Make sure you have gotten rid of hello.R from /R and /man


Make sure your License: is filled in with something.

Once you've gotten it to run without error when using :

document() load_all() build() and check()

Make sure in your .gitignore file, you have the following:

```
.Rproj.user
.Rhistory
.RData
```

This basically stops GitHub from putting pushing heaps of useless files 

Then you're read to put it on github.

I open the GitHub desktop, and then go to the top left corner and add a repository, I then 














