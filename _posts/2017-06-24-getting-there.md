---
layout: post
title: Getting there!
tags: [status-update]
author: Pradyun Gedam
---

Midway into week 4, work is going along at a brisk pace.

## Work Done

A fair amount of work got done.

- #59 has been closed. An upgrade-all command would be discussed once this GSoC project is completed.
- Clean up the pip codebase and add a new imports-sorted CI job
- Initial part of Stage 2 of the proposal (moving all cache handling into pip.cache) has merged.

## Work Ongoing

There's a lot of other improvements that are ongoing.

- Adding mypy integration into pip's codebase
- Adding a new Required-by to pip show
- Supporting forward slashes on Windows, when installing local directories
- Adding man pages to pip
- Updating pip's documentation related to configuration
- Adding the ability to autocorrect a user's mis-typed command
- Final part of the "Goal" of Stage 1 is basically ready

## What next?

As Stage 1 is pretty much done, I'll look into additionally further breaking down the current `pip.resolve` module to make it easier to work with. This would be a big help coming into Stage 3.

Regarding Stage 2, adding a `pip.cache` module to pip, it is indeed underway. 
