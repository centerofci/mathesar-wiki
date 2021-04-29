---
title: Code Review Guidelines
description: 
published: true
date: 2021-04-29T19:52:19.539Z
tags: 
editor: markdown
dateCreated: 2021-04-29T17:28:01.167Z
---

# General Advice
- Commit early, commit often.
- Write good commit messages.
- Create draft pull requests for in-progress work.
- Try to keep pull requests small if possible, since it makes review easier.

# Review Process
Please follow these guidelines when reviewing PRs.

## Authors
- Once you think your code is ready to merge, mark your draft pull request as "ready for review" or create a pull request if you don't have a draft. The required reviewers will automatically be notified when you do this.
- Please post in `#mathesar:matrix.org` and tag the Mathesar maintainers (`@blm`, `@pavish`, `@kgodey`) when you have a PR ready for review.
- If the reviewer requests changes, please make the changes and **re-request review**.
- Do not resolve comments, let the reviewer do this.

## Reviewers
- Check for outstanding PRs at the start of your day.
- Request changes if you want another look at the PR before it is merged.
- Resolve your own comments, do not resolve anyone else's.
- If you approve the PR, merge it unless someone else has requested changes.
- If the branch needs to be updated before merging (because it's out-of-date with the master branch), do so, as long as the action can be performed automatically.  Otherwise, ask the Author to handle it.
- Always merge using merge commits, never squash or rebase (the GitHub interface should disable squash and rebase, but check just in case).

# Reading
Some reading related to our process:

## Why not squash or rebase merges?
- [Why I’m against merging pull requests in squash mode or rebase mode?](https://myst729.github.io/posts/2019/on-merging-pull-requests/)
- [Sqauash merges are evil](https://medium.com/bananatag-engineering-blog/squash-merges-are-evil-171f55139c51)
- [Why git squash merges are bad](https://felixmoessbauer.com/blog-reader/why-git-squash-merges-are-bad.html)
- [Git merge - to squash or not to squash? - Stack Overflow](https://stackoverflow.com/questions/26999930/git-merge-to-squash-or-not-to-squash)

## Commits
- [Commit early, push often](https://www.worklytics.co/commit-early-push-often/)
- [Commit message guidelines](https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53)