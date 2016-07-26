creating an r package from scratch again.

I don't really like using the RStudio "create R package" GUI, as it creates a new function, "Hello.R", which you have to delete from the /R directory and the /man directory. Not a huge inconvenience but a little annoying.

```
devtools::create("/Users/tierneyn/Google Drive/ALL THE THINGS/PhD/code/R/vizdat")
```

Make an R script.

get the roxygen skeleton. I use a snippet to do this.

write the function code.

Make sure you have imported the function you need using @import.

If you are only using one function from a package, consider using @importFrom 

```
#' @importFrom tidyr gather
```

document it: `devtools::document()`

build it: `devtools::build()`


check it: `devtools::check()`

I got the error: 

```
* checking package dependencies ... ERROR
Namespace dependencies not required: ‘dplyr’ ‘ggplot2’ ‘tidyr’

See section ‘The DESCRIPTION file’ in the ‘Writing R Extensions’
manual.
* DONE
Status: 1 ERROR

```

Which is a reminder to make sure if you use a package in your file, you must put it in the description. You can ensure that this is done in the right way by typing `devtools::use_package()`, 

So in my case, for `vizdat`, I used: 

```
devtools::use_package("ggplot2")
devtools::use_package("tidyr")
devtools::use_package("dplyr")
```

doc, build, and check it.

Then you're good to go!

Next steps:

Fill in the description.

Create a README.

This 