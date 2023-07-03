# Intentional Git Kata

**Conquer the fear of Git!**

Practice and understand Git operations like rebase, interactive rebase, and others ... **all in a safe environment.**<br>
Break it. Fix it. Reset it. Build your intuition. Create new habits. Get confident in your workflows.

Most importantly: **Have fun!**

____________

### Prerequisites:

- Basic familiarity with Git for everyday use (branch, merge, commit, pull, push).
- A local clone of this repository. Please check out the existing feature branch as well as `develop`.
  You can ignore the `main` branch for this exercise.

**Before we begin:** *We assume that we have not yet pushed our local feature branch. If we had already pushed, we might
handle it differently depending on the situation; in that case, make sure you understand the consequences
and/or ask your Kata organizer or trainer. In general, clean up before pushing, and rebase frequently.*

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

Rebase your local branch onto the recent changes on `develop`.<br>
(Optional: First merge/pull develop into your branch to see what the graph would look like, then
reset your branch to the previous state before rebasing, and compare the results.)

## Exercise 3

#### Scenario

You are ready to open a pull request for your current changes, but first you have another
quick look at your change set. One commit catches your eye: "Fix typo in previous commit."
That's a bit ugly. It doesn't add any value to the commit history and only makes it harder
for future maintainers to understand the decisions that led to the final result. Luckily a
colleague just introduced you to interactive rebase.

#### Task

Squash those two commits together so that the typo in the code is fixed and only the commit
message from the meaningful commit is kept.

## Exercise 4

#### Scenario

There is another occurrence of multiple commits that should really be one, but there are
other commits between them. If someone were to check out the first one, baited by its
commit message, they would get an inconsistent state of the code base.

#### Task

Use interactive rebase to squash those commits together, only keeping the meaningful commit message. Hint: You might need to fix the order of some of the commits first.

## Exercise 5

#### Scenario

So far the program prints "Hello World!". In the next step we want to enhance the `Greeting`
to allow for dynamic greetings like "Hello Universe!" or "Hello \<name\>!". We want to do
this in a TDD fashion.

> **Tip 1**<br>
> When developing using TDD, we can regard each "green" phase (i. e. tests pass) as
a checkpoint. If we create a commit as soon as the tests are green and then we mess
something up (e. g., during refactoring), we can easily go back to the last green state at
any time. After the refactoring phase, if the tests are still green, we can either create
another commit or amend the previous one, based on good judgment and the size of
the refactoring.

#### Task

a) Add your unit testing library of choice. Which library and version do you prefer, and
why? Make sure to explain your choice in the commit message.

> **Tip 2**<br>
> Choosing JUnit 5 because it is the most recent version at the time? Or choosing
JUnit 4 because the team is more familiar with it? If you decide to document
that information, the commit history is the best place for it. A future maintainer
who is confused by the use of one version over another can search for "JUnit 4"
and quickly find the reason behind the decision. In a wiki, this info could get lost
or quickly become obsolete.

b) Using TDD, implement the new functionality described above in the simplest way
possible. As soon as the tests pass, create a commit.

> **Tip 3**<br>
> If you struggle with a habit of committing at the end of the day or randomly from
time to time instead of intentionally committing consistent intermediate states,
consider writing the commit message first. It's a trick to increase intentionality
and foresight.

c) Refactor, then create another commit. Now a full "red-green-refactor" iteration is
finished. Consider squashing the last 2 commits if the intermediate state before the
refactoring step does not add any value on its own and is now obsolete as a "checkpoint".

___

© 2023 Raimund Krämer - Use with attribution.

Links to third party sites are included for convenience only and I am not responsible for their contents.
