---
title: 'TIL: Adding Policies in Cisco Firewalls'
author: Edel
type: post
date: 2017-01-05T05:26:38+00:00
url: /networking/til-adding-policies-in-cisco-firewalls/
categories:
  - Networking
tags:
  - firewalls
  - work

---
Identify traffic with an access-list

<pre>access-list <em>acl-name</em> permit ip <em>source</em> <em>destination</em> dscp <em>dscp-value</em></pre>

Apply the access-list with the dscp value to an interfact

<pre>class-map match-all <em>interface</em>
match ip dscp <em>dscp-value</em></pre>

Apply the policy

<pre>policy-map <em>map-name</em>
    class <em>class-name</em>
        [bandwidth <em>bandwidth-value</em>]
        [priority <em>priority-level</em>]
        set ip dscp <em>dscp-value</em></pre>

Today at work I was going over firewalls. We want to check the configuration of the firewalls and compare them to our QoS standards. I&#8217;m not too familiar with how policies and QoS are implemented on Cisco devices so it was pretty interesting to learn.