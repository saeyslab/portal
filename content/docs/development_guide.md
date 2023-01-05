+++
title = "Development Guide"
description = "Development guide"
date = 2025-05-01T08:00:00+00:00
updated = 2021-05-01T08:00:00+00:00
sort_by = "weight"
weight = 2
template = "docs/page.html"
+++

## Adding datasets

There are multiple ways to add a dataset:

- Add to the `www/` the IRC NextCloud
- `cp` or `rsync` directly to `fs4.irc.ugent.be`
- `sshfs` the `www/` locally and `rsync` to it.

Example workflow at our lab's work machine:
```
rsync -aT data/my_dataset /auto/net/irc/fs4/www/flow
```