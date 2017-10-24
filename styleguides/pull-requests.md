# Pull requests

This is a pull requests style guide for working on Barnardo's Digital projects.

## Why we do pull requests internally

* It's good to have a second opinion
* It's good to spread the knowledge and socialise changes with others
* It's good to notify people who aren't directly involved but who can help
  with an `@name` mention   

## Things to remember

* It's your job to request a review and get your changes merged 
* A PR doesn't have to be all of the work - it's okay to have follow-up PRs for a
  feature if a set of changes are complete enough to go live

## Guidance for each step

If you are not sure how to do any of this, please feel free to ask for help.

### Opening a request

* Rebase to master frequently so your changes can be merged conflict-free
* Your title and description help the reviewer. Make the title succinct
  and descriptive, and then add as much detail as you like in the description.
* The description should summarise your changes and include useful links, eg to
  an associated issue, post, or related PR. If the changes involve
  the frontend, we love screenshots!
* Github emails the title and description of the PR to those following
  the repo when you raise it. Further changes aren't emailed, so it's worth 
  spending a bit of time getting it right first time
* Explain or highlight any changes you think are contentious, and any testing 
  that you've already done
* If you use fixups (and why wouldn't you? Fixups are a 
  [wonderful time-saver](https://robots.thoughtbot.com/autosquashing-git-commits))
  make sure you squash them out of existence before you open the PR –
  because the comment is necessarily not related to the fix, it takes extra 
  effort for a reviewer to parse
  

Note: The canonical description of changes should always be in the individual
commits - PRs are GitHub-specific, and we would lose that history
if we switched (or Github went) away. Please read 
[commit message style guide](/git.md#commit-messages).

### Reviewing a request

#### Guidelines for review

The review stage is as important as writing the code in the first place. Give
it the time it deserves. This is the part with people and feelings in it. We
respect one another's efforts, and we're liberal with praise (when something's
good, we *say so*!).

- Be kind. Your choice of language is important. Prefer 'we' to 'you' – the unit of
  delivery is the team, and we take collective responsibility for our work
- If you're not sure how the committer wants their request reviewed, ask them
  before starting - they may prefer some of the feedback to be done in person
  or while pairing
- Try not to use the "changes requested" function in Github for now, unless
  the committer has indicated they're ok with it. Big red crosses don't do much
  for your day. We can get better outcomes than the review tools with kindness 
  and respectful language

#### Let other reviewers know what you're doing

- If you're going to discuss some issues offline, please let people know in the
  PR so that no-one merges in the meantime. "Please don't 
  merge, discussing offline" is enough. When that conversation has taken place 
  elsewhere, summarise the result as a comment on the PR for the benefit of 
  others. Do this as soon after the conversation as you can so that you don't
  lose context
- If you look at a PR but don't feel comfortable merging it please say what
  you've looked at or not so other reviewers know the review isn't finished
  yet
- If you're committed to reviewing the request through to merging or closing,
  assign the PR to yourself

#### Helpful things to consider while reviewing

- Take the changes for a test drive - even if the tests pass it might have bugs
- Consider security when reviewing code, and always where there is user input.
  The [basic security guidance](TBD.md) might help
- Remember that a PR does not have to entirely solve the problem. If it adds
  value on its own it is better to merge now rather than wait for the rest of
  the changes required
- Try to comment on individual lines in the full-file diff view, not on a commit
  page. Github loses them if you rebase
- Ensure that any relevant documentation (`README` files, things in the `doc`
  folder) is up to date with the changes
  
#### What if we're reviewing our own work?

This happens a bit in small teams – you pair on a thing and then there's no-one
to review it who hasn't already worked on it. Sometimes reviewing your own work
is unavoidable, but in these circumstances, open the PR, then walk away for a day.

When you both come back to review the PR, you'll probably notice things that
weren't obvious when you opened it. The time and space away from it is 
tremendously useful for avoiding merging things that you notice later aren't
quite right.  

### Addressing comments

Address any comments flagged as blocking. This includes spelling or
grammatical errors in documentation.

- If you're changing something minor in an existing commit (eg renaming a
  variable for clarity, adding a missing test), rewrite or amend the existing 
  commit with a rebase (we can help if you're not sure how to do this)
- Major changes addressing feedback can be addressed in a separate commit 
  that follows the [commit guidelines](git#commit-messages)
- Explicitly comment that all relevant comments have been addressed to notify
  watchers. You can use the "approve" function in the GitHub review tools  
- Major refactoring can and should be done in follow-up pull request - it
  is never a blocker
  
### Merging a pull request

Once you're certain that there are no blocking comments, merge through Github.
By default this creates a merge commit, and this is our default (as opposed to
rebasing onto master, which would create a seamless commit history with no
evidence of the feature branch). If you're offline and merging manually, use
`git merge --no-ff` to get the same behaviour and preserve evidence that the
feature branch existed.