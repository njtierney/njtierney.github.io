---
title: Other little customisations for jekyll
layout: post
comments: true
---

# Creating the right kind of RSS for r-bloggers

Thanks to alex-singleton for his [blog post explaining this]()

# 

# Making images 100% width

Simply add the following code to the .css

```
```

As I have done in [/....css]()


# Adding LaTeX to jekyll.

Turns out this isn't super hard - thanks to [this blog post](http://cushychicken.github.io/easy-latex-in-jekyll/), and by proxy, [this SO post](), 

You just need to add the following code to the top of your _layouts/post.html file:

```
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
```

As I have done [here]()

# Making Accordian headers for the Resources page

Source the JS at the top of the page

```
<!-- load up the jquery script needed for the accordian -->

<head><script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.1/jquery.min.js"></script></head>
```

Include the JS

```
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

```

And then, unfortunately, you write the accordians inside HTML tags. I'd love to work out a way to add an expansion or package to markdown so I can write some sort of syntax around it. But...that would take (an unnessary amount of) time.

# Making "Anchor" links for the headers

Basically, [download the anchor.min.js](https://bryanbraun.github.io/anchorjs/), and then [source the JS in default.html]()

```
<script src="{{ site.baseurl }}/public/anchor.min.js"></script>
    <script type="text/javascript">
    anchors.options.placement = 'left';
    anchors.add();
    </script> 
```

And add the following code in the [lanyon.css]()

```
/* Add the anchor.js CSS so that it fades in */
.anchorjs-link {
  transition: all .25s linear;
}
```

# Typography

Adhering to Butternick's rules, I changed the linespacing to 145%,...




