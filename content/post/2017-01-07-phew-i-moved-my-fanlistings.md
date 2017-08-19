---
title: Phew… I Moved My Fanlistings
author: Edel
type: post
date: 2017-01-07T14:50:11+00:00
url: /websites/phew-i-moved-my-fanlistings/
categories:
  - Websites
tags:
  - fanlistings

---
Fanlistings are basically the early 2000&#8217;s version of Facebook pages. I [own a bunch of them][1], mostly of songs or video game characters. Honestly, the whole fanlisting thing has been going down in popularity as the years go by. It&#8217;s a bit sad. Fanlistings come and go a lot. There&#8217;s a high turnover rate. I try my best to maintain and keep mine up and running.

However, my old domain name expired and I had trouble getting in touch with my registrar to renew it. I really loved that domain name because it featured my frequently used user handle but I determined it to be a lost cause and ultimately let it go. Since GitHub introduced the student pack which included a .me domain for free for one year, I claimed it. Hence, _edelgrace.me_ was born.

Right now I&#8217;m using $50 credit from [Digital Ocean][2] (yes, that is a referral link) for an Ubuntu droplet. However, it only runs on 512MB RAM so I opted to buy a cheap 1GB RAM server from [RamNode][3] (no, that is actually not a referral link). 512MB RAM would probably be enough for me since I don&#8217;t receive many visits to my websites but you never know what the future might bring.

So on the event of my domain expiring, I moved all of my fanlistings over to the RamNode server. I exported a SQL file through phpMyAdmin from my website to recreate the database and ran it on the server. Since I wanted better naming conventions, I had to change all the config files in order to connect to the database. There were some issues that I had to plow through in Enthusiast, one being that the absolute path to the fanlisting script needed to be changed. Since I&#8217;m no longer of thinking of sticking to hosting but rather maintaining my own servers, I don&#8217;t think I should have to worry about changing the path ever again.

Afterwards, I had to contact [The Fanlisting Network][4] (TFL) in order to change my URLs. The network is to ensure that duplicate fanlistings don&#8217;t exist. In theory, duplicate fanlistings can exist but the ones listed on TFL are more trusted.

In summary, that was my evening last night. It took up more time than I wanted but that&#8217;s okay. I still managed to get some studying for CCNA done so all went well.

 [1]: http://fan.edelgrace.me
 [2]: https://m.do.co/c/999dd787b62c
 [3]: http://ramnode.com
 [4]: http://thefanlistings.org