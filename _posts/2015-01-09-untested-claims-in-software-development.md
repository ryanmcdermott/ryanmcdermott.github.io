---
title: Untested Claims in Software Development
author: Ryan McDermott
layout: post
permalink: /untested-claims-in-software-development/
categories:
  - Uncategorized
---
When I became a developer professionally, I was nervous that I would be unable to keep up with conversations with other developers. The first time I walked into a developer conference I sincerely expected to be of a mindset that wasn&#8217;t scientifically and mathematically rigorous enough. You see I came from a background more steeped in Liberal Arts and other rather soft studies. It wasn&#8217;t until talking with other developers for a while that my opinion of my own prospects began to change. Indeed, I was impressed by how brilliant many of the programmers I talked to were, but I was equally struck by how utterly opinionated I found the milieu of the software development world to be. Things weren&#8217;t black and white &#8212; there weren&#8217;t simply just hard truths and blatant lies. Many assertions made weren&#8217;t even corroborated by any experiment or formal proof. I expected to hear more conversations like this:

> This algorithm is of O(n) time complexity

> This code will use X bits of memory

> Y amount of power will be consumed on this embedded systems application over Z units of time

Instead what I heard were conversations that were more like this:

> X text editor will make you a better programmer

> Y coding style is the best way to write code

> Z is the best language

I don&#8217;t mean to indict developers and the community at large. Software is far more subjective than it is objective, despite the mathematical underpinnings of computer science. After all, we call it &#8220;writing&#8221; code for a reason. Moreover, I don&#8217;t mean to cast all conversations in a bad light. I did hear and still often do hear talks that are like the first set of quotes rather than the second.

However, what I do intend to indict is the zeal by which we can make claims that really aren&#8217;t tested or proven. Debates are certainly good, and we should suss out the truth in everything we can in the world. But when we have conversations like the first set of quotes above, all we can do is talk *at* each other and exchange anecdotes, either vociferously or cordially. While I&#8217;m pretty convinced that Vim is a really fantastic text editor and not having to use a mouse as frequently makes **me** a &#8220;better&#8221; developer, I can&#8217;t claim that would be true for **all** developers. After all, some people love Emacs! Perhaps a formal study could prove my claim one way or another, but in the end, by making unproven claims we are taking a little of the science away from the study of computer science.

What should we do then? How can we resolve a problem that seems so intractable? Well for one, I think we need to be honest with ourselves about where our claims are grounded. Have they been proven, in the same way that merge sort&#8217;s time complexity has or, are they merely beliefs we have gathered over our years of professional experience?

Second, I think more empirical studies are in order. There have already been quite a few, such as one regarding [ if camelCase or underscores][1] are easier to read. A lot of claims can be formally tested and terms can be operationally defined, despite what a tall order that may seem. We can apply some rigor to the word &#8220;better&#8221; when we talk about what makes for a better developer. We can truly settle debates about if Agile development is the best way to go. And, we can have more assurance that our design patterns will truly be productive and not just a continuation in a long line of uncontrolled experiments. While the new year is still fresh, my wish is to improve not just our skills and our codebases, but our mindset about software development. At the very least, maybe we can all agree on that!

 [1]: http://ieeexplore.ieee.org/xpl/articleDetails.jsp?reload=true&arnumber=5521745