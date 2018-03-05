---
layout: tutorial
title: Git Workflow Best Practices
subtitle: How to contribute code effectively
category: Developer
index: 1
---

# Git workflow

The core branches of the `RevBayes` repo that should always exist are

-   `master`
-   `development`

The `master` branch should always reflect the state of the current release of
`RevBayes`.
The `development` branch should contain the working additions/changes to the
code that are to be included in the next release.
Under normal circumstances, you should not work on either of these branches
directly.
Rather, to make changes or work on a new feature, you should create a separate
branch off of `development`.
While working on your branch, frequently merge changes from `development` to
stay up to date.
Once your work is ready, and *before* you merge your branch into `development`,
make sure to merge any changes from `development` and verify the code is
compiling and tests are passing.
Never merge a feature branch directly into `master`, the only exception being
hotfixes to the current release.
For hotfixes, create a separate branch from `master`, make the fix and verify
it, and then merge the hotfix branch into `master` and `development`.

A great reference:

-   <http://nvie.com/posts/a-successful-git-branching-model/>

## Cleaning up feature branches

