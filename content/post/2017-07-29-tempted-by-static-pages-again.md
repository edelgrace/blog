---
title: Tempted by Static Pages Again
author: Edel
type: post
date: 2017-07-29T14:01:27+00:00
url: /programming/tempted-by-static-pages-again/
categories:
  - Programming
  - Websites

---
I recently started learning how to use [emacs][1], which is a text editor and a Lisp interpreter. During my quest for resources, I came across a number of developers and their blogs. Since I&#8217;m always intrigued by what sort of tools developers use to make their blogs, I did a little snooping. A shocking number of people who didn&#8217;t use WordPress as their blogging platform opted for flat files instead.

Now I had dabbled a little bit in static pages before with [BoltWire][2] but ultimately abandoned it to go back to WordPress. I think where I went wrong with BoltWire was that it simply did not have a big enough community (although they are an extremely dedicated community) to keep me reassured that I had made the right choice.

However, I know flat files in general is a real and upcoming thing. Since I&#8217;m planning to use emacs and Markdown files as my main way of documenting things, it would be easy to use it in my blogging as well.

So my main reasons for switching to a flat file system:

  * **Better security**  
    WordPress was giving me so much trouble when it came to security. Yes, Jetpack did help in reducing spam and MySQL doesn&#8217;t randomly stop working anymore but you have to admit that using WordPress on a Digital Ocean server makes you a target.</li> 

  * **Version control**  
    Yes, WordPress does have versioning for content however it would be much easier to have version control for settings, themes, etc. over the WordPress kind.
  * **Less bloat**  
    I don&#8217;t need everything that WordPress offers and honestly sometimes I feel like it might be a bit overkill. Since the server I&#8217;m on has limited RAM and disk space, I need to be careful about the amount of resources I use. It helps that I don&#8217;t have many visitors to begin with but still!
  * **Faster loading times**  
    While I&#8217;m unsure if this is too much of a concern for me but loading times do make me a bit worried. Fetching from a database can be quite slow.
  * **I want a more future proof blogging system**  
    There are options to export your content into XML files in WordPress however it can&#8217;t beat readable Markdown, which many static file systems use. The fact that everything is file based is future proof in itself. Migrating from one server to the other wouldn&#8217;t be too much hard work.

My concerns:

  * **What comment system to use**  
    I do not like Disqus. I dislike the fact that I have to register for yet another site and people can&#8217;t click on my name on a comment and go directly to my website. I also don&#8217;t like the fact that the comments don&#8217;t stay on my server. I want to be able to have my comments.
  * **Learning curve**  
    This would be a little more technically involved at first to get everything installed, just due to the nature of it not being a one-click install.
  * **So many choices!**  
    There is no shortage of flat file systems out there. Like I&#8217;ve said, I&#8217;ve dabbled in BoltWire before and wiki systems but it&#8217;s so hard to find one that will work for you when there&#8217;s a breadth of options.

One of the main frameworks I&#8217;ve been looking at is [Hugo][3] which is used by [Baty.net][4], [Modern Emacs][5], [kieranHealy.org][6], [but she&#8217;s a girl&#8230;][7], and more. I am very attracted to this option because it seems like it could work pretty well with an emacs workflow.

Thankfully, I finally recovered my previous website, [erzadel.net][8] and now have access to my old blog posts. I&#8217;ll be tinkering with that this weekend and try to have a clone of my old blog up and running on my local machine. We&#8217;ll see how it goes!

 [1]: https://www.gnu.org/software/emacs/
 [2]: https://www.boltwire.com/
 [3]: http://gohugo.io/
 [4]: https://baty.net/
 [5]: http://www.modernemacs.com
 [6]: https://kieranhealy.org
 [7]: http://www.rousette.org.uk/blog
 [8]: http://erzadel.net