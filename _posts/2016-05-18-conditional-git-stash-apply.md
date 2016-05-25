---
layout: post
title:  "Conditional Git Stash Apply"
date:   2016-05-18 21:00:00 -0400
categories: tips-and-tricks git
comments: true
analytics: false
permalink: /blog/tips-and-tricks/git/conditional-stashing
---

We've all been there. You've researched GitFlows, you've gotten a process down that involves issues queues, branches and pull requests. But you've done the unspeakable: you've started work on multiple features outside of branch management. How do we go back? How do we separate our work and keep our flow intact?
<!--more-->

As a developer, I believe that Git is one of the most powerful tools in my daily rotation, and that `git stash` is one of my most frequented Git commands. Whether I am reviewing someone else's code, preventing partial commits on incomplete features, or just trying to troubleshoot a piece of functionality, `git stash` allows me to quickly jump between code states without losing work or committing low-quality code to the repository.

In this post, I'll discuss another useful feature with `git stash`, which is the capability to conditionally apply stashed code changes based on specific file needs. Historically, when you apply a `git stash`, you are applying everything in the latest version of a stash, or a specified stash index to the current branch (Note: You may also apply the stash index directly to a new branch. For more on that and other stash capabilities, see [git-scm](https://git-scm.com/book/no-nb/v1/Git-Tools-Stashing)).

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

**Stashing our initial changeset:**

~~~ git
$ git stash;
$ git stash show;
~~~

**Applying the first set of feature changes to a new branch:**

~~~ git
$ git checkout -b "feature-branch-first";
$ git checkout stash@{0} -- path/to/file.name
$ git add path/to/file.name
$ git commit -m "First feature branch changes."
~~~

**Applying the second set of feature changes to a new branch:**

~~~ git
$ git checkout -b "feature-branch-second";
$ git checkout stash@{0} -- path/to/file.name
$ git add path/to/other/file.name
$ git commit -m "Second feature branch changes."
~~~

And it's as easy as that. Of course, you'd probably want to perform a `git merge` between your branches to ensure the code carries along the same state, but overall you are ready to reunite your work with your team's feature branch workflow.