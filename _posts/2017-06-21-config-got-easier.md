---
layout: post
title: Configuration just got easier!
tags: [new-thing]
author: Pradyun Gedam
---

This week, pip just grew a new command - `pip config`. Here's a peek into how it looks...


```
$ pip config list
list.format = legacy
$ pip config edit  # opens in your default editor, needs --editor if it can't
$ pip config get list.format
legacy
$ pip config set list.format columns
$ pip config get list.format
columns
```

## Wait, why?

pip allows the use of configuration files and environment variables to set any non-default behavior that you may want. There are 3 places from where pip loads configuration files - site-wide, per-user and virtualenv-specific - with later files overridding the previous ones. These files are stored in OS-specific directories.

`pip config` is meant to assist with the management of these configuration files. It allows you to list the contents of a file, open the file in your favorite text editor to edit manually and even get/modify/remove configuration values directly from the command line.

`pip config` modifies only one file in one run - if the user does not specify which one then pip tries to determine which is the most appropriate file to utilize. If you're in a virtualenv, pip would use the virtualenv-specific file otherwise it uses the per-user file. The file being used can be overriden the using CLI options: `--user`, `--global`, `--venv`. 

<sub>PS: I have a feeling pip 10.0 is gonna be pretty sweet. :)</sub>
