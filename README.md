# Intentional Git Kata

**Conquer the fear of Git!**

Practice and understand Git operations like rebase, interactive rebase, and others ... **all in a safe environment.**<br>
Break it. Fix it. Reset it. Build your intuition. Create new habits. Get confidence in your workflows.

Most importantly: **Have fun!**

____________

### Prerequisites:

- Basic familiarity with Git for everyday use (branch, merge, commit, pull, push).
- A local clone of this repository. Please check out the existing feature branch as well as `develop`.
  You can ignore the `main` branch for this exercise.

**Before we begin:** *We assume that we have not yet pushed our local feature branch. If we had already pushed,
we might handle it differently depending on the situation, which we will not cover here. In general,
clean up before pushing, and rebase frequently.*

_____________

## Exercise 1

#### Scenario

You just committed your changes, but only afterwards you realized that you mistyped the
ticket ID in the commit message (`ABC-43` instead of `ABC-42`). This is worse than most
typos since it can be actually misleading for future maintainers (including yourself).

#### Task

Amend the commit to fix the ticket ID in the commit message.


## Exercise 2

#### Scenario

When you created your branch you branched off from `develop`. In the meantime a colleague
has merged their pull request (ticket `ABC-32`) into `develop`. Pulling those changes into
your branch and then targeting develop with your PR can lead to a messy commit graph,
which is worsened the more features are being developed in parallel.<br>
Instead we aim for a more linear commit history, where branches do not outlive multiple
other merges or are mixed together. We care about the **intention** behind the commits
and about the **information** they provide, not about the accidents and coincidents that
happened along the way.

#### Task

Rebase your local branch onto the recent changes on ‘develop’.
(Optional: First merge/pull develop into your branch to see what the graph would look like, then
reset your branch to the previous state before rebasing, and compare the results.)
