git-branch-name-checker
=======================

Prefixing ticket number to each of the commit is a good
idea. Automating it would take 1 thing out of our mind so that we can
focus on our real task.

There are two things in this repo:

- commit-msg

  a git commit message hook that firstly checks the branch name, if it is
  SEAL compliant (in the format of SEAL-NNN-your-description), it will
  check the commit message and see if it has the prefix already, if it
  doesn't it will prepend it automatically.

  to use it, drop the the commit-msg file to .git/hooks/ in your git
  repository. It needs to be executable.

- git-seal-branch

  a git extension which we can use to create a branch, it will
  complain if the branch name isn't SEAL compliant (in the format of
  SEAL-NNN-your-description).

  to use it, add it to PATH and run:

  ```
  git seal-branch your-branch-name
  ```
  It needs to be executable.


