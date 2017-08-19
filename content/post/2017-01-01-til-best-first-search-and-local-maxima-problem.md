---
title: 'Private: TIL: Best First Search and Local Maxima Problem'
author: Edel
type: post
date: 2017-01-02T06:40:16+00:00
draft: true
private: true
url: /programming/til-best-first-search-and-local-maxima-problem/
categories:
  - Programming
tags:
  - AI
  - algorithms
  - TIL

---
Okay, this wasn&#8217;t the first time I learned about this but I did relearn this while talking to my SO about the AI textbook he was reading.

There&#8217;s a concept called best first search. The basic example is traversing through a tree. Each node that the algorithm visits, it adds the node to an array solely for visited nodes. It keeps another array for nodes it hasn&#8217;t yet visited. While it traverses through the nodes, it sorts the visited node array so that the best node is at the start of the array.

This does pose the problem of local maxima. The best search first algorithm gives the best result at that moment for the current search space. So it doesn&#8217;t focus on efficiency but reducing the search space. This doesn&#8217;t guarantee the best solution at any point in the search but the best solution for that point of time in the search (if that makes any sense at all).