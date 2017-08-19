---
title: 'Python: Cookies and Requests'
author: edel
type: post
date: 2016-10-29T01:47:03+00:00
draft: true
private: true
url: /2016/10/python-cookies-and-requests/
categories:
  - Knowledge Base
  - Programming
tags:
  - python
  - 'python: requests'

---
<pre>import requests

cookie = r.cookies['cookie_name']
cookie = { 'cookie_name': cookie }

requests.post(url, cookies=cookie)</pre>

<ol class="footnote">
</ol>