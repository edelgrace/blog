---
title: Silly Mistakes
author: Edel
type: post
date: 2016-10-31T22:04:29+00:00
url: /life/silly-mistakes/
categories:
  - Programming
  - Work

---
At work I'm writing a simple script in Python that pulls data from a sqlite database. I was doing some inserts and deletes and I was wondering why the database wasn't changing. I tried printing out the queries and double checking that they were indeed correct syntax-wise. I traced my program line by line up to the point where queries were being executed. Finally, I turned to Google.

Stackoverflow, of course, delivered. "Did you commit your database?"

Oh. My. God.

I forgot to save the database after making all the changes. For some reason I was grinning ear to ear, thinking "I'm so stupid" in my head. The project manager was walking by my desk and looked at me weirdly.

I know for sure I'm not making that mistake again!


