---
title: 'Security By Obscurity: Just Hide It?'
author: Edel
type: post
date: 2016-06-07T03:26:11+00:00
url: /life/security-by-obscurity/
categories:
  - Technology
tags:
  - security

---
Last semester I took an introductory course to information security. One of the concepts we touched on was "security by obscurity." Basically what that means is if no one is aware of something, they can't possibly break into it. For example, hiding your diary is a form of security by obscurity. Of course, this has it flaws. There is always the possibility that someone could somehow stumble upon your diary by accident. There might people actively looking for something valuable to you but they won't know what it is until they find it. Notice I didn't mention "if" they find it. It's always a good practice to assume that they will find it. This is one of the reasons why security by obscurity is not ideal.

Truth be told, I use security by obscurity. The diary analogy I used was something that I actually do. Now, my mom loves to poke around and I still live with her. She has read my diaries in the past so it's not far-fetched that she would find my diary one day and read it. This is why I don't use it as my only form of security. My journal entries are either about really mundane stuff or encrypted with [Elian script][1]. So unless my mother is good at cracking ciphers (which I highly doubt as English is her second language and frequency analysis is probably lost on her), I can safely assume that my secrets are safe with me.

The reason why I suddenly started thinking about this is because I have a project that I've been working on. I've been trying to build a book management script. Right now I'm just finishing up simple features for the admin panel such as tagging a book, adding a review to a book, editing author names, etc. All of this is currently in a folder with an obscure name. At first I thought that if my admin folder wasn't named something obvious like "admin," I would less likely have a security breach. Who would want to hack my tiny and unpopular websites anyway? Then I realized, wait, that's a really bad idea.

Curious, I looked up if there was a way to discover folders that were not explicitly linked publically. I was not surprised when I saw that such a way does indeed exist. In fact, there are several ways (or programs) to do this. Software like [URL Fuzzer][2] and [DirBuster][3] utilize a method called fuzzing. In my introductory class, we would classify this as a brute force method. What fuzzing does is try any possible number of combinations in order to find a weakness. In this case, it tries to find out if a folder exists. Specifically, DirBuster goes through a list of words (have not checked if it includes random strings or just common words) and appends them to a URL. Depending on the HTTP status code (things like 404 not found or 403 forbidden), it can determine if a folder exists on the website or not.

So, knowing this, I could still use security by obscurity. However, like my diary, I plan to implement other layers of security. Whether or not it will increase security or just give it security it didn’t have in the first place, I’m not sure (entropy wasn't my strong point in my information security course). But I am sure that leaving it as a randomly named folder is not the way to go. I know how to do simple PHP sessions with a login but only with matching the submitted password with a plaintext password in a database. That's a whole other realm of security issues so I'm going to start reading up on hashing passwords in PHP. I've poked around some open source scripts and have found MD5 hash functions so that's probably what I'm aiming for. Honestly, I'm not well-versed in web security specifically (other than SQL injections are bad and you have to sanitize them) but that’s why I’m still learning.

So the next time you think you’re just going to hide something and think you’ll be fine, you probably will be but it’s better if you combine it with some other security technique especially if it contains sensitive information.




 [1]: http://www.ccelian.com/concepca.html
 [2]: https://pentest-tools.com/website-vulnerability-scanning/discover-hidden-directories-and-files
 [3]: http://git.kali.org/gitweb/?p=packages/dirbuster.git;a=summary