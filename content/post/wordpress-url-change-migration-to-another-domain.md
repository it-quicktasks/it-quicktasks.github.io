---
title: "Wordpress URL change upon migration to another domain"
date: 2019-09-28T23:17:11+08:00
tags: [wordpress, migration, url-change, domain, change]
draft: false
---

The easiest is to add it to "wp-config.php". Something like:

```
define('WP_HOME','http://NEW_DOMAIN.com/');
define('WP_SITEURL','http://NEW_DOMAIN.com/');
```

You can test from 'curl' it it works:
```
curl -IL http://NEW_DOMAIN.com
```
