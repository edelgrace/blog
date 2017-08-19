---
title: 'TIL: How to Add a MySQL User'
author: edel
type: post
date: 2017-01-03T04:14:55+00:00
url: /programming/til-how-to-add-a-mysql-user/
categories:
  - Programming
tags:
  - mysql
  - vps

---
<pre>CREATE USER 'user'@'server' IDENTIFIED BY 'PASSWORD';
GRANT PRIVILEGES ON database.table TO 'user'@'server';</pre>

I recently bought a VPS from Ramnode and started tinkering on it. I needed to create a database for my fanlistings. Back when I was on shared hosting, I would use cPanel and phpMyAdmin to do all that. This is admittedly another TIL that I didn&#8217;t learn today but, rather, relearned today because the information slipped my mind. Maybe I need to rename this little segment to &#8220;TIRL.&#8221;