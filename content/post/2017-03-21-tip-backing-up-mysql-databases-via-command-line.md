---
title: 'Tip: Backing Up MySQL Databases Via Command Line'
author: edel
type: post
date: 2017-03-21T19:26:59+00:00
url: /programming/tip-backing-up-mysql-databases-via-command-line/
categories:
  - Programming
tags:
  - mysql

---
`</p>
<pre>mysqldump -u username -p database > backup_name.sql</pre>
<p>`

I always forget this command. I always try to attempt to go `mysql dump` instead of `mysqldump`. Hopefully posting this little blurb will give me an easy reference in the future!