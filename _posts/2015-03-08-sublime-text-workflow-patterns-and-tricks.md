---
title: Sublime Text Workflow Patterns and Tricks
author: Ryan McDermott
layout: post
permalink: /sublime-text-workflow-patterns-and-tricks/
dsq_thread_id:
  - 3578043653
categories:
  - Uncategorized
---
<div>
  Editors are personal choices, just like a lifestyle, tradition or philosophy. As with those things, there are no right and wrong choices. There are only suggestions that may or may not be helpful to you. Pick what works for you and don’t listen to naysayers that make judgments based on what helps you the most. Having said that, here’s my list of development workflow patterns that I use with my editor of choice, Sublime Text 3:
</div>

  * **Use Vintageous.** It’s super helpful. It allows you to use Vim commands within Sublime. Serious Vim users won’t find everything there, but it employs the 80/20 of Vim nicely (80% of what I need is there from the 20% of Vim’s features) <https://github.com/guillermooo/Vintageous>
  * **Use a large monitor.** For one it’s annoying to try to click through tabs and separate windows. Additionally, it’s been shown to increase productivity. <http://gbr.pepperdine.edu/2010/08/three-ways-larger-monitors-can-improve-productivity/>
  * **Use columns.** I’m a full-stack guy so I typically have to deal with writing server-side code as well as front-end code at the same time. I split up backend and front end files into separate columns in the editor. In Sublime this can be achieved by going to View -> Layout -> Then selecting the amount of columns you desire. I typically use two, one side for front-end, one side for backend.
  * **Use a different themes.** I prefer Spacegray. <https://github.com/kkga/spacegray/> Take a look at this for more ideas: <https://scotch.io/bar-talk/the-best-sublime-text-3-themes-of-2014>
  * **Use Source Code Pro**. In my opinion, it does a bit to enhance readability over the default Courier New: <https://www.google.com/fonts/specimen/Source+Code+Pro>
  * **Use plugins.** Picks one that are relevant to what your needs are, but by far the one that applies to everyone is the Package Control plugin: <https://packagecontrol.io/browse/popular>
  * **Use a project file** and exclude certain files and folders from search. It also helps you boot directly into your code base.
  * **Use Sublime as a terminal command. **You can boot a project file or just Sublime directly by the ‘subl’ command. Enable it with this: 
    <pre><code data-language="Bash">
ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" ~/bin/subl</code></pre>

  * **Use a startup script **to boot a VM if you use one and certainly to load the Sublime project files.
  * **Use some helpful keyboard shortcuts. **My most used are:** **Command + P to search through files in your project. Command + Shift + ] to go to the tab to the right. Command + Shift + [ to go to the tab to the left. Check out the full list: [http://sublime-text-unofficial-documentation.readthedocs.org/en/latest/reference/keyboard\_shortcuts\_osx.html][1]
  * **Use Multi line select**. Hold the Alt key and then drag your mouse up and across the lines you want to edit.

<div>
</div>

<div>
  Leave me a comment with some more ideas based on your experience with your preferred editor.
</div>

 [1]: http://sublime-text-unofficial-documentation.readthedocs.org/en/latest/reference/keyboard_shortcuts_osx.html