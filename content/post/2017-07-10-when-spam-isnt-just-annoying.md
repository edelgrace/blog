---
title: When Spam Isn’t Just Annoying
author: Edel
type: post
date: 2017-07-10T17:16:00+00:00
url: /websites/when-spam-isnt-just-annoying/
categories:
  - Websites

---
The past couple of weeks I noticed that the MySQL service on my server would routinely stop out of the blue. At first I suspected that it was because my 512MB RAM wasn&#8217;t enough but when I looked at the usage history, I never peaked more than 9%. I even tried reinstalling the MySQL server which worked at first but then it stopped running again.

However, I think the problem was due to bots trying to log into my WordPress dashboard. One thread I was reading suggested xmlrpc attacks were bringing WordPress down. When I looked at my logs, there was a dozen of attempted logins.

There are multiple solutions for this, mainly blocling xmlrpc but since I use third party apps that rely on xmlrpc, I didn&#8217;t want to block it entirely. Jetpack was another solution which is what I eventually opted for.

I&#8217;ve been wary of installing Jetpack, mostly due to the fact my server is not that great and I was worried about space and memory consumption. However, it does have a feature to block malicious xmlrpc login attempts that I desparately needed.

It&#8217;s only been two days now (as of writing this) and I already see that Jetpack has blocked over 25 login attempts. Now this doesn&#8217;t protect me from other attacks and on other sites on this server but at leaat I have that out of the way.