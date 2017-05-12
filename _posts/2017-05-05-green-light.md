---
layout: post
title: It's the Green Light!!
tags: [status-update]
author: Pradyun Gedam
redirect_from: "/2017/05/05/green-light/"
---

I have been selected as a student in GSoC 2017 - one of the 1,318 students worldwide! It's a pretty awesome feeling. I'm looking forward to the work in the coming months!

## Overview of the proposal

My proposal is for fixing pip's dependency resolution - by implementing backtracking dependency resolution within pip. The project would have essentially 3 stages:

- **Refactoring**: Mostly breaking apart the God classes within pip's codebase.
- **Preparation**: Implement Dependency Caching and move all caching code into one module.
- **Implementation and Testing**: Actually implement a backtracking dependency resolver.

The full proposal text can be found [here][proposal-gist].

## Community Bonding Period

I have examinations from 10th May till 25th May. Thus, I would be fairly inactive during the Community Bonding period. The exception to this would be the week of 15th May. I would have a 9 day break before my "Data Structures and Algorithms" paper - I should be able to get to some time in that week to try to clear out my existing PRs to pip on GitHub.

I guess, that's all there is for now. :)

[proposal-gist]: https://gist.github.com/pradyunsg/5cf4a35b81f08b6432f280aba6f511eb
