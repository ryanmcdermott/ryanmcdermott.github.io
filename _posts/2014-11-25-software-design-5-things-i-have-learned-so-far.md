---
title: 'Software Design: 5 Things I Have Learned So Far'
author: Ryan McDermott
layout: post
permalink: /software-design-5-things-i-have-learned-so-far/
dsq_thread_id:
  - 3259881597
categories:
  - Uncategorized
---
Over the last few years of developing software professionally I&#8217;ve gathered up a few insights based on my experiences. These don&#8217;t apply to every kind of project or company, but in general I hope they are helpful.

# 1.

<address>
  <em>When dealing with user accounts, make users part of an organization.</em>
</address>

It&#8217;s easy to assume that just an individual user is going to be registered for the usage of your application and that will be that. It&#8217;s trivial to implement &#8212; most frameworks have a built-in or third-party authentication plugin for handling what ends up being individual user registration. This is great to solve the problem at hand for most apps, however as your application grows, it&#8217;s very possible that you will want to include multiple users along with associated permissions. There&#8217;s little harm in having an organization as a first-class citizen and users as second.

# 2.

<address class="p1">
  <em><span class="s1">Any data integrity or security checks you do in the client must also be done on the backend.</span></em>
</address>

<p class="p1">
  This seems very obvious at first, but if you are going to limit functionality on a user level basis, or as per having a login session token, then limits placed on the client API calls must also be placed server-side as well.
</p>

# 3.

<address class="p1">
  <em><span class="s1">Know what can be cached and what can&#8217;t.</span></em>
</address>

<p class="p1">
  If your app is making expensive calls and manipulations on data from your RDB or even NoSQL database, a caching strategy should be used.  Caching though is a hard solution though, to what is superficially an easy problem &#8212; too many database calls. To implement caching effectively you must also implement <a href="http://en.wikipedia.org/wiki/Cache_invalidation">cache invalidation</a> properly, and as the saying goes, cache invalidation is one of the hardest problems in computer science. A simple strategy for some apps is to cache transient, yet hard to compute data, and refresh it at a fixed interval. This won&#8217;t work for every application so it&#8217;s important to consider your own unique design requirements.
</p>

# 4.

<address class="p1">
  <em><span class="s1">Use deleted codes for entries instead of deleting rows.</span></em>
</address>

<p class="p1">
  Quite often, a user will erroneously delete some of their data and they will want it back. Instead of doing DELETE FROM <em>table_name </em>WHERE <em>some_column</em>=<em>some_value</em>; it can be better to simply UPDATE a table with a column that is called something like status_code. When you are retrieving rows from your RDB, simply check for rows with an active status code. This also creates a nice design pattern that lets you set all sorts of different properties of your data, other than just DELETED.
</p>

<p class="p1">
  I should note, this insight does not apply to all applications &#8212; if you are dealing with very sensitive consumer data and are dealing with HIPAA, PCI, or any of the myriad regulations out there, then this may not be the best idea. Also, if you are dealing with a high volume of relational data, you may not want to preserve everything that is no longer needed. Notwithstanding this, there are many good reasons to simply UPDATE a status_code column, as opposed to calling a SQL DELETE command.
</p>

# 5.

<address class="p1">
  <em><span class="s1">Languages and frameworks can be productivity enhancements, but they don&#8217;t solve the hard problems for you.</span></em>
</address>

<p class="p1">
  Every time the sun comes up it seems a new framework rises with it. MVC frameworks can solve many of the basic problems of application development, and certainly they should always used. The biggest problems though in designing software aren&#8217;t going to be addressed by a new framework or a fresh new language. Quite often actually, not using a tried and trusted technology stack can actually introduce more problems. The biggest challenges you will face will be in actually creating an application to fulfill your customer&#8217;s needs. Sure scaling will be an issue, but that&#8217;s one of those good problems to have &#8212; it means you&#8217;re solving a lot of people&#8217;s problems. For the meantime, use something that works, even if it isn&#8217;t that sexy.
</p>