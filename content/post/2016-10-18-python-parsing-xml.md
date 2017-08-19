---
title: 'Python: Parsing XML'
author: Edel
type: post
date: 2016-10-19T01:56:22+00:00
draft: true
private: true
url: /life/python-parsing-xml/
categories:
  - Knowledge Base
  - Programming
tags:
  - python
  - xml

---
<pre>import xml.etree.Element as ET

# from string
root = ET.fromstring(string)

# from file

tree = ET.parase(file)
root = tree.getroot()</pre>


