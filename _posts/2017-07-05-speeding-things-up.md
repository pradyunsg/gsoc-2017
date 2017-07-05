---
layout: post
title: Speeding Things Up!
tags: [status-update]
author: Pradyun Gedam
---

I got added to the PyPA Github Organization! YAY!

The past few days of work have mostly resulted in incremental improvements to pip's codebase and supporting infrastructure.

pip's CI infrastructure which took as much as 50 minutes to run automated tests on the codebase got an overdue improvement, resulting in some sweet gains.

## Work Done

- Went through quite a few of pip's issues 
  (no idea what the count is, between 70 and 120 I guess)
- Improved CI builds for pip - builds now take 20 minutes or less
- Much needed documentation update for pip config was made
- pip show got a new Required-By field
- pip install now supports forward slashes on Windows
- pip install now shows where it's looking for packages when using non-default 
  locations to find packages
- A new pip.operations.prepare module has been created further break up the 
  responsibilities of RequirementSet, as it was earlier

## Work Ongoing

- Autocorrection of mistyped commands
- Displaying a warning when pip installs a binary outside of PATH
- Improving AppVeyor CI
- Simplification of tox jobs
- Fixing the handling of namespace packages in pip 
- Populating RequirementPreparer (part of new pip.operations.prepare) with more 
  attributes from RequirementSet
- mypy integration for pip's codebase
- Discussion on introducing a `--scheme` option to pip for improving the 
  situation with installation schemes and modeling them more cleanly

## What next?

Coming into week 6, ideally, I should have had a working implementation of the sdist cache by now but that is not the case. Since I have another week to finish the implementation, I think I should be able to catch up on it in this week. I intend to stay on schedule and not touch the 2 week buffer in the project proposal's timeline.
