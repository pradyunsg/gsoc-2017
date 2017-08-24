---
layout: post
title: Wrapping up GSoC 2017
tags: [final-submission]
author: Pradyun Gedam
---

This is my final post as a part of GSoC 2017 and will serve as my "Work Product Submission".

I’m very grateful to both my mentors, Donald Stufft and Justin Cappos. They have been extremely responsive and helpful, even at odd times of their day. It has been a wonderful experience to have worked under the guidance of such awesome people through the summer.

## What work did I do?

The work done during GSoC 2017 has been refactoring pip's codebase and, occasionally, doing bug-fixes and implementing new features. The main deliverable of the project - implementation of a backtracking resolver - has not been completed; the refactoring work has taken longer than expected and there's still some that I'd like to do. Refactoring, moving code around and decoupling a fairly entangled codebase where there is a fair amount of action at a distance has been an interesting experience.

A short summary of the non-trivial work that I have done:

- Add a `pip config` command
  - Involved decoupling of Configuration related code to a separate module, which was partly done before GSoC started.
- Add man pages for pip
- Implemented autocorrection of mistyped commands in pip 
  - pip won't have this since it is not very easy to undo actions done by pip
- Improve CI times and make CI runs less flaky
  - They're still flaky; due to a pytest bug
- Add infrastructure support for checking import order 
  - Consistency across the codebase is nice
- Lots of refactoring and rewriting:
  - A new pip.resolve module
  - A new pip.operations.prepare module
  - A new pip.cache module
- Removed redundant code due to the refactoring + Py2.6 support drop
- Introduce infrastructure for YAML based tests
  - These are useful for testing that the resolver works
- Implement an sdist cache (it currently only caches egg-info)
  - Improving this to cache everything sdist is on my list
- Triaged 261+ issues and PRs
  - Formalized labels to categorize the same and tagged them

If, for some reason, someone wants to look into exactly what I've done as a part of GSoC, here's a [GitHub search][involved-search] of issues and pull requests I was involved in during the community bonding period and working period and all the [commits] made to pip in the same time frame.

### What about the resolver?

There was one deliverable in my project proposal - that pip would get a dependency resolver by the end of GSoC. I have not achieved that. 

https://en.wikipedia.org/wiki/Hofstadter%27s_law

This has been due to the fact that the logic for which package and version gets installed was (and still partially is) spread out across multiple modules and sub-packages within pip. Bringing together all of that logic into a single module has been more effort than I had anticipated. There's still some parts of the codebase that have to be modified substantially to implement the dependency resolver in a reasonable manner within pip.

I do have an overall algorithm for the resolver planned out and written down; it's not been tested with a whole host of real world situations though.

## So, what's next?

Until I finish adding a dependency resolver in pip, I'm going to hold off working on the other improvements that I have in mind for pip. My intent from the start of the project has been that when pip 10.0 comes out, it should have a resolver in it.

I think I will be posting at least 2 more entries on this blog - one to announce the addition of the resolver to pip and another to document and describe the structure of the resolver.

[involved-search]: https://github.com/pypa/pip/issues?utf8=✓&q=involves%3Apradyunsg%20updated%3A%3E2017-05-01%20updated%3A%3C2017-08-29
[commits]: https://github.com/pypa/pip/graphs/contributors?from=2017-05-01&to=2017-08-29&type=c
