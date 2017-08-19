---
title: 'TIL: How to Set Up Virtual Hosts on Apache'
author: Edel
type: post
date: 2017-04-02T17:50:31+00:00
url: /websites/til-how-to-set-up-virtual-hosts-on-apache/
categories:
  - Websites
tags:
  - apache
  - virtual hosts

---
**Create a virtual host configuration file _site-name.conf_ for the site:**

    sudo vim /etc/apache2/sites-available/<em>site-name.conf</em>

Inside the file:

    <VirtualHost *:80>
        ServerAdmin <em>email</em>
        ServerName <em>domain name</em>
        ServerAlias <em>domain name</em>
        DocumentRoot <em>path to folder no slash at the end</em>
        ErrorLog <em>path to error log</em>
        CustomLog <em>path to access log</em>
    
        <Directory />
            Options FollowSymLinks
            AllowOverride All
        </Directory>
    </VirtualHost>

**Add the site to the host file:**

    sudo vim /etc/hosts

Inside the file:

    127.0.0.1 localhost.localdomain localhost
    127.0.0.1 stashofyarn.ca stashofyarn

**Enable the site:**

    sudo a2ensite <em>site-name.conf</em>

**Reload the Apache service in sudo mode:**

    sudo service apache2 reload