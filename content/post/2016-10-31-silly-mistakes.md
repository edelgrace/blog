---
title: Silly Mistakes
author: edel
type: post
date: 2016-10-31T22:04:29+00:00
url: /2016/10/silly-mistakes/
categories:
  - Programming
  - Work

---
At work I&#8217;m writing a simple script in Python that pulls data from a sqlite database. I was doing some inserts and deletes and I was wondering why the database wasn&#8217;t changing. I tried printing out the queries and double checking that they were indeed correct syntax-wise. I traced my program line by line up to the point where queries were being executed. Finally, I turned to Google.

Stackoverflow, of course, delivered. &#8220;Did you commit your database?&#8221;

Oh. My. God.

I forgot to save the database after making all the changes. For some reason I was grinning ear to ear, thinking &#8220;I&#8217;m so stupid&#8221; in my head. The project manager was walking by my desk and looked at me weirdly.

I know for sure I&#8217;m not making that mistake again!

<ol class="footnote">
</ol>