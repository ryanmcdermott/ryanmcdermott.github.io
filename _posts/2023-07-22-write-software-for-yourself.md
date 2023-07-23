---
title: Write Software For Yourself
author: Ryan McDermott
layout: post
---

I was chatting with a colleague about life outside of the office. The usual
stuff came up: family, hobbies, exotic vacations. I jokingly asked him,
"but what about code?" He dryly replied, "I don't program outside of work."

At lunch the next day my curiosity piqued. After the table assembled, I asked:
"do any of you write software outside of this place?" My coworkers were a bit
amused and several chimed in that they didn't think about work outside of work.

I understood the sentiment. That's how I used to feel too. As an employee
of a Big Tech co, it's easy to justify leaving what _looks_ like work _at_
work itself. And you're paid well enough to not need the résumé signal or 
the proof of ability that is entailed in publishing open source code or
demonstrating your side business to the world.

But there's a lot more to developing software than just the code you produce.
There are the obvious things: improving your skills, gaining GitHub stars,
connecting with a community, feeling proud of your accomplishments. But there 
is also something more subtle that does not get mentioned. When you develop your 
own software you also develop your personal values in the process.

For me, this was most apparent when I was looking for a way to edit encrypted
documents on my local machine. I wanted to record passwords and other personal
data, and with that sensitivity came the need to be certain of **exactly** the code 
that was running over my data. The vast majority of what I saw had loads of
dependencies, and many required interfacing with browsers or other native UI
libraries, many of which could break or disappear in a few decades.

I wanted something I could rely on forever, for documents that I would always add 
upon and come back to. So I decided to make my own encrypted text editor. Sort of to 
learn but mostly to follow a wild intuition about how I could improve things.

As I started writing the program, I realized I had a strong philosophy
about what I wanted to instill in all of the applications that I create:
* Made with boring tools.
* Minimal dependencies, internally vendored if I need any at all.
* Runnable for as long as possible, ideally forever.

The final product of this was a terminal text editor I use regularly,
called [Ette](https://github.com/ryanmcdermott/ette).

Your ideas don't have to be so modest though. People start immensely successful
companies from what began as humble side projects. Software has the power 
to create worlds out of nothing. We are orchestral conductors of little crystals 
of sand. We can make them dance to any tune we choose.

So give it a try. Write software for yourself. Even if it's just a helpful 
one-liner. You might just learn something about yourself along the way.