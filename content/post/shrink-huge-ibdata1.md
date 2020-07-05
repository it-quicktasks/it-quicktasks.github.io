---
title: "Shrink Huge ibdata1"
date: 2019-11-24T23:15:37+08:00
tags: [mysql, mariadb, innodb, optimization]
draft: false
---

Best way is to make one file per table and not use default which baloons to a huge file and never shrinks when some tables are removed and unused.
See https://www.thegeekstuff.com/2016/02/mysql-innodb-file-per-table
