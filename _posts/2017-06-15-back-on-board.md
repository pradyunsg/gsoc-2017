---
layout: post
title: Back on Board!
tags: [status-update]
author: Pradyun Gedam
---

I missed the mandatory blog post in the previous fortnight. Whoops. Here goes...

## Work Done

The first stage of the project - refactoring `RequirementSet` is well underway; the [primary PR][PR-4526] adding a `pip.resolve` has been merged. Following this a few smaller PRs will be made improving the use of `pip.resolve` throughout the codebase and also reducing the amount of things `RequirementSet` does.

Another major thing that was merged in just yesterday is a new configuration command for pip - `pip config`. I'll be making a blog post about this soon.

Other work includes:

- fixing random issues in the tracker, while waiting for the CI to complete
- improving the CI infrastructure + adding a CI job for import sorting
- readablilty improvements in parts of the codebase

Part of the reason I haven't done a lot is because I had taken a week off, as informed earlier to the mentors and in accordance to what I wrote in my proposal.

## Work ahead

By the time this fortnight is done, Stage 1 has to be completed. This would mean a lot of small changes here and there in the codebase. It might get a little tight so I'm going to pull up my socks.

As yet, there have not been any behaviour changes to pip install - this would change starting week 4, when new behaviours would be added to pip install.

[PR-4526]: https://github.com/pypa/pip/pull/4526
