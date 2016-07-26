---
title: Resources
layout: post
categories: 
- R
- Statistics
---

There are a lot of questions and answers on the internet. This page lists resources that I have found useful, so I thought you might find them useful too.


<!-- load up the jquery script needed for the accordian -->

<head><script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.1/jquery.min.js"></script></head>

<!-- JS -->
<script type="text/javascript">
  $(document).ready(function($) {
    $('#accordion').find('.accordion-toggle').click(function(){

      //Expand or collapse this panel
      $(this).next().slideToggle('fast');

      //Hide the other panels
      $(".accordion-content").not($(this).next()).slideUp('fast');

    });
  });
</script> 
<!-- End JS -->

<!-- HTML -->
<div id="accordion">
<h1 class="accordion-toggle">Starting out with R</h1>
<div class="accordion-content default">

<p>
Step one: <a href="https://cran.r-project.org/">download R</a> to your appropriate system (Windows, Mac, and Linux).
</p>

<p>
Step two: <a href="">download RStudio</a>. Trust me, RStudio makes using R much much easier.
</p>

<p> 
If you are having problems with getting R or RStudio, check out <a href="https://github.com/fawda123/swmp_installR/blob/master/R_install_guide.pdf">this guide</a>, from <a href="https://beckmw.wordpress.com/2014/09/28/back-to-square-one-r-and-rstudio-installation/"> this guy</a>. It covers installing R and RStudio in a little more detail.
</p>

</div>


<h1 class="accordion-toggle">Learning and Troubleshooting with R</h1>
<div class="accordion-content">

<p>
To learn R, you need to learn <a href="">how to get unstuck with R.</a>
</p>

<p>To learn a new function or package head to:</p>

<ul>
<li> <a href="http://www.statmethods.net">Quick-R</a>, which provides nice quick description of functions and aother R-things.</li>
</ul>

<p>For all my other problems, I usually google the error code, or search at 
<a href="http://stackoverflow.com">StackOverflow</a> </p> 

<p>I would also recommend checking out:</p>

<ul>
<li>RStudio's <a href="http://www.rstudio.com/resources/training/online-learning/#R">list of resources for learning R</a>, and</li>

<li><a href="http://www3.nd.edu/~mclark19/projects.html">This blog post</a>, which describes learning R from a social sciences background</li> 
</ul>
</div>


<!-- start another accordian -->
<h1 class="accordion-toggle">Learning Advanced R</h1>
<div class="accordion-content">

<p>Got a basic handle on R and are hankering for more? I recommend these two (free, online) books by Hadley Wickham:</p>

<ul>
<li> <a href="http://adv-r.had.co.nz">Advanced R Programming</a></li>

<li> <a href="http://r-pkgs.had.co.nz">R Packages</a></li>
</ul>

<p>There is also this new book which seems similar(ish) to Hadley's books:</p>

<ul>
<li> 
<a href="http://www.quantide.com/R/r-training/r-web-books/ramarro-r-for-developers">Ramarro</a> 
</li>
</ul>

</div>

<h1 class="accordion-toggle">Advanced R stuff: S3 Classes</h1>
<div class="accordion-content">

<p>
S3 classes are this really awesome minimal class of functions that can be super handy in R. They are described nicely in Hadley's book, but I have also found these to be helpful:
</p> 

<ul>
<li> <a href="http://www.cyclismo.org/tutorial/R/s3Classes.html">This R Book</a>, which is also an entire book on R programming.</li>

<li> <a href="http://abhishek-tiwari.com/hacking/class-and-objects-in-r-s3-style">This blog post</a>, which also has such a suave blog layout ... Just sayin'.</li> 

<li> <a href="http://www.youtube.com/watch?v=VZkD7DXQ-fk&amp;feature=g-upl">This video by Dr. Andrew Robinson.</a> Slides are also available <a href="http://files.meetup.com/1685538/presentation.pdf">here.</a> Thanks to <a href="http://damjan.vukcevic.net">Damjan Vukcevic</a>) for this information.</li>
</ul>

</div>

<h1 class="accordion-toggle">Data Visualisation</h1>
<div class="accordion-content">
<p>
`ggplot`

If you are going to do a plot in R, it should be in ggplot. The standard graphics in base R have a _slight_ advantage in speed , but ggplot's `qplot` takes care of that.

My rule: if I spend more than 2 lines of code for a plot in base R, I will switch to ggplot. Actually, scrap that, I just use ggplot now. The only exception is when I use an S3 plot.`specific package` function.

OK, so why use ggplot? It follows a logical syntax adapted from the book "The Grammar of Graphics". It makes visualisation make sense. And there are lots of other packages that build upon it to make it more awesome, such as GGally.

So here are some ggplot resources:

- [This handout](http://www.ceb-institute.org/bbs/wp-content/uploads/2011/09/handout_ggplot2.pdf) provides an introduction to ggplot.
- [The ggplot index](http://docs.ggplot2.org/current/index.html) The ggplot index page is usually where I head to first off when I want to understand how to add and build upon my graphs.
- [The R Graphics Cookbook](http://www.cookbook-r.com/Graphs/) is also really nice.
- I also recently discovered the [ggplot2 wiki](https://github.com/hadley/ggplot2/wiki), which has some great case studies and examples.
- The [RStudio ggplot cheatsheet](https://www.rstudio.com/wp-content/uploads/2015/05/ggplot2-cheatsheet.pdf) is also really nice. It sits pinned up on my desk.

### ggvis

ggvis is another great package which builds upon the structure of ggplot but it allows for more interactive, reactive, plot building. Examples can be found [here](http://ggvis.rstudio.com/0.1/quick-examples.html) [here](http://ggvis.rstudio.com/ggvis-basics.html), and [here](http://ggvis.rstudio.com/cookbook.html).

### Shiny

shiny is a really awesome way to enhance your R plotting, and turn them into 'apps' (although whether they are actually apps is questionable, in my opinion).

- [shiny](http://shiny.rstudio.com/tutorial) tutorial
- [shiny cheatsheet](http://shiny.rstudio.com/articles/cheatsheet.html)
- [super awesome example](http://shiny.rstudio.com/gallery) here

</p>
</div>

<h1 class="accordion-toggle">Data Manipulation</h1>
<div class="accordion-content">

- Use [dplyr](https://github.com/hadley/dplyr) to manipulate data in R. [Here is a helpful lesson](http://www.dataschool.io/dplyr-tutorial-for-faster-data-manipulation-in-r)
- Use [tidyr](https://github.com/hadley/tidyr) to melt data (new version of `reshape2`)
- Use [broom](https://github.com/dgrtwo/broom#broom-lets-tidy-up-a-bit) to create **tidy dataframes** of statistical models. [Here is a helpful lesson](http://127.0.0.1:22465/session/Rvig.15c681ac18b1d.html)

</p>

</div>


<h1 class="accordion-toggle">Reproducible Reporting</h1>
<div class="accordion-content">

<p>
Probably the coolest thing ever. `knitr` is this amazing package that allows the user to combine their code and document text, making research easier to reproduce, and it does this while looking slick and classy. The idea is essentially to let the human do the writing, and the computer handle displaying the results, so that reports can be easily constructed, and most importantly, reproduced easily.
</p>

<p>
Check out some really nice guides [here](http://rmarkdown.rstudio.com/) and [here](http://rmarkdown.rstudio.com/html_document_format.html), and from the awesome dude who invented knitr [here](http://yihui.name/knitr/).
</p>

</div>



<h1 class="accordion-toggle">Learning R and Statistics</h1>
<div class="accordion-content">

<p>
If you want to learn statistics using R, check out [this website](http://www.dataschool.io/15-hours-of-expert-machine-learning-videos) containing 15 hours of an applied R statistics course from Stanford. They also have an [excellent (and free!) book](http://www-bcf.usc.edu/~gareth/ISL/).
</p>

</div>
<!-- close accordian -->


<h1 class="accordion-toggle">Decision Trees</h1>
<div class="accordion-content">
<p>
I use decision trees a lot in R, and I even [wrote a little package](https://github.com/tierneyn/neato) that helps take care of some common tasks in interrogating decision trees. Here are a list of resources that I recommend using to learn about them:
</p>

<ul>
<li>
[This bookd from James et al](http://www-bcf.usc.edu/~gareth/ISL/ISLR%20First%20Printing.pdf) - chapter 8 specifically refers to decision trees. They've also made the book free! Also [their videos](https://www.youtube.com/playlist?list=PL5-da3qGB5IB23TLuA8ZgVGC8hV8ZAdGh) on decision trees are very useful. You can find a comprehensive list of all their videos and material at [this website](http://www.dataschool.io/15-hours-of-expert-machine-learning-videos)	
</li>

<li>
This [book chapter](http://mason.gmu.edu/~csutton/vt6.pdf) from the Handbook of Statistics is broad and general.
</li>

<li>
This [page](http://architects.dzone.com/articles/regression-tree-using-gini%E2%80%99s) helps explain regression trees. Their [gif](http://f.hypotheses.org/wp-content/blogs.dir/253/files/2013/01/gini-x1x2-x1-b.gif) demonstrating how decision trees choose splitting values is also really helpful.
</li>

<li>
[This video on](http://www.statsoft.com/Textbook/Boosting-Trees-Regression-Classification) introduction to boosting trees for regression and classification by statsoft.
</li>
</ul>
</p>
</div>

<h1 class="accordion-toggle">`STATA` Related Resources</h1>
<div class="accordion-content">

<p> STATA do a great job of explaining multilevel and hierarchical models on their blog. I found these two blogs and video really helpful: </p>

<ul>

<li> [Blog part 1](http://blog.stata.com/2013/02/04/multilevel-linear-models-in-stata-part-1-components-of-variance/) </li>

<li> [Blog part 2](http://blog.stata.com/tag/multilevel-models/)</li>

<li> [Video](https://www.youtube.com/watch?v=rUWT_EWV6QI) </li>

</ul>

</div>

<!-- Close Accordian -->

Massive thanks to [this fellow](http://uniondesign.ca/simple-accordion-without-jquery-ui/), whose code powers these nice little minimal accordian tabs