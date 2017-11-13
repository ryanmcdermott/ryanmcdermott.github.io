---
title: Docker and the Future of Software
author: Ryan McDermott
layout: post
permalink: /docker-and-the-future-of-software/
dsq_thread_id:
  - 3084208619
categories:
  - Uncategorized
---
Recently I started taking a look at [Docker][1] which aims to be the future of shipping software. I was skeptical at first but after watching several videos ([1][2], [2][3]) I was blown away by the possibilities and what this means for the future of software. The power of Docker is the ultimate abstraction from the underlying operating system.

We have been stuck in a model of tying all of our software dependencies and our applications themselves to the very same file system and package directories that our operating systems use. Keeping track of our development and production box&#8217;s installations of our app&#8217;s dependencies is not the kind of productive work we should be doing as developers. We should be focusing on our applications!

Realizing this observation about Docker struck me. I think we will look at the world before Docker much in the way we look at the world of literature before the printing press &#8212; everything was done by hand with far too much energy and subjected our work to a great deal of human error.

The other metaphor that strikes me is the one proclaimed by the Docker community, and is at the very core of its philosophy &#8212; that is *containerization*. With Docker, we realize that what we should be doing is specifying our app&#8217;s entire software ecosystem as a container, and not as a series of installations we need to do directly on the server that will be running our code. We should feel confident knowing that our local development boxes and every single on of our production boxes as well are using an identical setup, just as a civil engineer feels confident that her CAD mockups and physical simulation software maps exactly to the real world or a ship captain knows that the company&#8217;s goods will be handled identically on every ship and every port.

As the world&#8217;s computing needs grow, especially with the coming of IoT and the incredible volume of data that will arise from all of our sensors, we need scalable ways of keeping our software dependencies and applications in controlled and contained states. Docker is the best solution I see.

### My practical Docker example:

I was working on a quick side project and took the chance to create a Dockerfile for a Python 3 Flask App that uses uWSGI and Nginx. [Check it out on my GitHub project][4]

 [1]: https://www.docker.com/
 [2]: https://www.youtube.com/watch?v=Q5POuMHxW-0
 [3]: https://www.youtube.com/watch?v=pts6F00GFuU
 [4]: https://github.com/ryanmcdermott/docker-flask