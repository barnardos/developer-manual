# Pull requests

We use pull requests (PRs) internally because they're good for:

* getting a second opinion on changes
* spreading the knowledge and socialise changes with others
* notifying people who aren't directly involved but who can help with an `@name` mention

A PR doesn't have to be all of the work - it's okay to have follow-up PRs for a feature if a set of changes are complete enough to go live.

## Opening a request

When opening a pull request, you should:

* [rebase to master](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) frequently so your changes can be merged conflict-free
* make the title succinct and descriptive
* add as much detail as possible in the description
* use [keywords](https://help.github.com/articles/closing-issues-using-keywords/) within the description to close and reference other issues
* spend a bit of time getting the title and description right first time
* explain or highlight any changes you think are contentious, and any testing
  that you've already done
* squash [fix-ups](https://robots.thoughtbot.com/autosquashing-git-commits)) before you open the PR
* request a review as it's your responsiblity to get a PR merged

The canonical description of changes should always be in the individual commits - PRs are GitHub-specific, and we would lose that history if we switched (or GitHub went) away.

## Reviewing a request

The review stage is as important as writing the code in the first place. Give it the time it deserves. Be kind. Your choice of language is important. Prefer 'we' to 'you' – the unit of delivery is the team, and we take collective responsibility for our work.

When reviewing a pull request, you should:

* take the changes for a test drive - even if the tests pass it might have bugs
* consider security when reviewing code, and always where there is user input
* remember that a PR does not have to entirely solve the problem
* try to comment on individual lines in the full-file diff view, not on a commit page as GitHub lose comments on the commit page if you rebase
* ensure that any relevant documentation (`README` files, things in the `doc` folder) is up to date with the changes
* use GitHub's built-in approval system

### How to review your own work

This happens a bit in small teams – you pair on a thing and then there's no-one to review it who hasn't already worked on it. Sometimes reviewing your own work is unavoidable, but in these circumstances, open the PR, then walk away for a day.

When you both come back to review the PR, you'll probably notice things that weren't obvious when you opened it. The time and space away from it is tremendously useful for avoiding merging things that you notice later aren't quite right.

## Addressing comments

Address any comments flagged as blocking. This includes spelling or grammatical errors in documentation.

When addressing comments, you should:

* rewrite or amend the existing commit with a rebase if you're changing something minor in an existing commit (eg renaming a variable for clarity, adding a missing test)
* address major feedback in a separate commit
* explicitly comment that all relevant comments have been addressed to notify watchers
* move an major refactoring to follow-up pull request - it is never a blocker

## Merging a pull request

Once you have an approval, merge your own pull request through GitHub. By default this creates a merge commit (as opposed to rebasing onto master, which would create a seamless commit history with no evidence of the feature branch). If you're offline and merging manually, use `git merge --no-ff` to get the same behaviour.

Delete your branch after the pull request is merged.
