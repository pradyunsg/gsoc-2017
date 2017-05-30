---
layout: post
title: The Clock is Ticking!
tags: [status-update]
author: Pradyun Gedam
---

GSoC 2017 Working period has now started!

## Work Done

For the most part of the Community Bonding Period, I had my University Semester Ending Examinations - which meant that I only really got a week of actual working time during the Community Bonding Period. That said, it was definitely a productive week with a fair number of PRs merging and a good number of small (but annoying IMO) issues getting fixed.

## Work ahead

The first stage of the project - refactoring - will be what I'll be working on for the better part of the coming month. It's supposed to be a tricky task since the refactoring touches one of the more complicated (and critical?) portions of the codebase.

The aim is to reduce `RequirementSet` down to merely a class representing sets of packages and what operations have been taken upon them. While anything short of that is acceptable, The tentative short summary for this would be:

- Move out `prepare_files` into a separate `pip.resolve` module
  - Move only the relevant responsibilities into the new module
- Determine if adding a `pip.download` is useful and move the relevant functionality to it
- Move `install` related code out into `pip.operations.install` module
- Move `uninstall` related code out into `pip.operations.uninstall` module

There's some investigative work to be done related to actually figuring out how the intertwined parts of `RequirementSet` would be separated out and that's what I have all this time for. :)
