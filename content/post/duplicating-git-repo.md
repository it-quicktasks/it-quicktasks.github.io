---
title: "Duplicating a git repo"
date: 2018-04-08T23:17:11+08:00
tags: [git, version-control, repo]
draft: false
---

```
git clone --bare https://example.com/repo.git
cd repo.git
git push --mirror https://remote-example.com/repo.git
```

See https://help.github.com/articles/duplicating-a-repository/
