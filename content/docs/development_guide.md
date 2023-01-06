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

### NextCloud

Add to the `www/` folder in the [IRC NextCloud](https://cloud.irc.ugent.be/private/).

### SSH 
`rsync` directly to `fs4.irc.ugent.be`.

```
rsync -a --info=progress2 path/to/my_dataset benjaminr@fs4.irc.ugent.be:/srv/data.new/exp/units/u_ysa/private/www/new_parent_of_my_dataset
```

### SSHFS

Mount the remote `www/` folder locally with `sshfs`  and `cp` or `rsync` to it.

Setup:
```
sudo mount -t sshfs -o remount,allow_other,default_permissions -o Compression=no benjaminr@fs4.irc.ugent.be:/srv/data.new/exp/units/u_ysa/private/www /auto/net/irc/fs4/www
```

Example workflow at our lab's work machine:
```
rsync -a --info=progress2 data/my_dataset /auto/net/irc/fs4/www/new_parent_of_my_dataset
```

## Rsync options

- `-a` transfer the whole folder with correct permissions.
- `--info=progress2` give a general progress overview with transfer speed and estimated time left.
- `--delete` remove files in the target directory not in the source directory.