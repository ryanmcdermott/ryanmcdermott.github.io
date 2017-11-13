---
title: Marionette Code
author: Ryan McDermott
layout: post
permalink: /marionette-code/
categories:
  - Uncategorized
---
As much as we may all love spaghetti, we&#8217;ve all had our code called it at some point. There&#8217;s nothing more disheartening than looking at your work and realizing it&#8217;s spaghetti code. It conjures up the image of a cowboy coder gone rogue out on the plains spinning out spaghetti all over the place. OK, well maybe not exactly that!

We&#8217;ve all blustered at the accusation and rejoined heartily that X person does not know what they are talking about.  Well then, in the interest of accuracy what is spaghetti code? According to Wikipedia it is &#8220;a [pejorative][1] term for [source code][2] that has a complex and tangled [control structure][3], especially one using many [GOTOs][4], exceptions, threads, or other &#8216;unstructured&#8217; [branching][5] constructs.&#8221;<sup><a href="http://en.wikipedia.org/wiki/Spaghetti_code">1</a></sup>

Ok then, that seems to be quite an expansive definition and one that has more subjectivity than objectivity. However, there is a Potter Stewart moment when you look at code, think it&#8217;s spaghetti, because &#8220;you know it when you see it&#8221; <sup><a href="http://en.wikipedia.org/wiki/I_know_it_when_I_see_it">2</a><br /> </sup>

Regardless I want to introduce another idea, that&#8217;s not pejorative but merely a matter of fact about life &#8212; some code has to be ugly. Some code has to handle an unhealthy amount of conditionals. Some code needs hacks because the underlying ecosystem, problem domain, and/or platform is so fractured. This is what I call marionette code. And guess what, EVERY web developer has to deal with it.

What do I mean? Try writing an all-encompassing, browser agnostic, and all-viewports-friendly web application. There&#8217;s so many conditions to handle &#8212; window resizing, browser JS interpreter inconsistencies, hacks to move elements around, mobile/tablet tweaks in real-time outside of CSS, and other hacks to just get JS running. The list goes on. The point of all of this is that the ecosystem that you are working with is broken. IE of course is the most obvious offender. But moreover, the web app ecosystem is so fractured. There&#8217;s so much one has to do to handle every form factor and viewport. You might say this is a fact of life, and of course it is which I don&#8217;t mind, but the code that you end up writing can look a little ugly at times &#8212; no thanks in part to how ugly Javascript can be. No flame war intended by that statement <img src="http://ryansworks.com/wp-includes/images/smilies/simple-smile.png" alt=":)" class="wp-smiley" style="height: 1em; max-height: 1em;" />

So what do we do? I think it&#8217;s important to lay back and accept that no matter how much we pump our code through wonderful frameworks like Angular, Ember, or Backbone, we are going to end up with some stuff that isn&#8217;t pretty. That&#8217;s ok though. Every developer I&#8217;ve met realizes this, though my argument here is no straw man. What I&#8217;m intending to say though is we need to consistently remind ourselves that to move a marionette around it takes a lot of strings. When those strings get tangled though, you end up with spaghetti!

<img class="alignnone size-medium wp-image-184" alt="Spaghetti" src="http://ryansworks.com/wp-content/uploads/2014/01/spaghetti+with+meat+sauce11-300x200.jpg" width="300" height="200" />

 [1]: http://en.wikipedia.org/wiki/Pejorative "Pejorative"
 [2]: http://en.wikipedia.org/wiki/Source_code "Source code"
 [3]: http://en.wikipedia.org/wiki/Control_structure "Control structure"
 [4]: http://en.wikipedia.org/wiki/Goto "Goto"
 [5]: http://en.wikipedia.org/wiki/Branch_(computer_science) "Branch (computer science)"