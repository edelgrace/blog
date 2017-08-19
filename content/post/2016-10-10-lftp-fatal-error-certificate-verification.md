---
title: 'LFTP Fatal Error: Certificate verification'
author: edel
type: post
date: 2016-10-11T01:48:31+00:00
url: /2016/10/lftp-fatal-error-certificate-verification/
categories:
  - Internet
  - Programming
  - Technology
tags:
  - git-ftp
  - lftp

---
### The error:

<code class="multi">~$ git-ftp pull&lt;br />
~$ cd: Fatal error: Certificate verification: certificate common name doesn't match requested host name ‘ftp.mazohyst.org’&lt;br />
~$ mirror: Fatal error: Certificate verification: certificate common name doesn't match requested host name ‘ftp.mazohyst.org’</code>

### Solution:

Edit `~/.lftp/rc` so that it contains `set ssl:check-hostname no`. What this does is pretty self explanatory. If the hostname in the certificate does not match the hostname you&#8217;re attempting to connect to, it doesn&#8217;t matter because it won&#8217;t check for that in the first place.

### The context:

I recently wanted to implement version control for my websites because all too often I think to myself, &#8220;I wish I knew what a previous version of this file looked lik&#8221;. So since I&#8217;m on shared hosting and don&#8217;t have my own server, I resorted to using [git-ftp][1] for deploying my websites. So far, it&#8217;s working great. However, I momentarily forgot I started using this and made some changes on one of my pages through cPanel. I tried pulling the latest pages using `git-ftp pull` and encountered this error.

### Sources:

  * [LFTP FTPS and Certificate Verification][2]

<ol class="footnote">
</ol>

 [1]: https://github.com/git-ftp/git-ftp
 [2]: http://web.archive.org/web/20160330173659/http://www.versatilewebsolutions.com/blog/2014/04/lftp-ftps-and-certificate-verification.html