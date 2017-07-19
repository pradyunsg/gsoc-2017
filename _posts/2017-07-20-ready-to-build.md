---
layout: post
title: Ready to Build!
tags: [status-update]
author: Pradyun Gedam
---

In the second half of the working period, I'll finally directly work on the new backtracking resolver for pip. 

Another semester of college has begun which meant that I've had to more things happening through the day than I did during summer vacations. While the amount of time I've had available for working on the project has reduced, there has still has been more than enough to keep my work schedule on track - which it is now.

## Work Done

- Finalize PR adding infrastructure support for using mypy in pip's codebase.
- Misc bugfix
- Improvement of pip.cache to encourage more code reuse between the existing wheel cache and the sdist cache.
- Finished the sdist cache implementation
- Read and looked in fair detail at the algorithms operating in existing resolvers - `Stork` and `pip-compile`
  - _might do a blog post on this topic this week, if it's useful_

## Work Ongoing

- Breakup requirement preparation routine into smaller pieces
  - Will be followed up by reducing coupling between `Resolver` and `RequirementPreparer`
- Get the sdist cache actually merged into master
  This is actually now overdue but I believe it's pretty much done so this should no longer be an issue.
- Implementation of a testing bed for the resolver
  - using YAML file based fixtures
- Looking into speeding up test suite

## What next?

In the second half of the working period, I'm going to avoid doing side-tasks and dedicate the majority of my working time on actually implementing a good backtracking dependency resolver. Essentially any new work that I think of doing related to improving the code quality, the support infrastructure of the project, adding new features etc will be deferred until the resolver is implemented.

Nearly all the preparatory work for actually implementing a resolver within pip is now done or awaiting feedback. Over the past few days, I've understood some interesting edge cases of the resolution problem and I am looking forward to (finally!) implementing the resolver in the remainder of the working period.


