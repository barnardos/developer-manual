# Branches

Branches are _yours_. You can do what you like to them – including [force pushing](https://git-scm.com/docs/git-push#git-push---force-with-leaseltrefnamegt) unless you've agreed with someone else that you won't.

This makes it easy to help your fellow developers by [rewriting](http://git-scm.com/book/en/Git-Tools-Rewriting-History) your commits regularly so that they make logical sense. You can use `git rebase --interactive` to do this.

Although it's sometimes hard to be disciplined, prefer smaller commits, which can be squashed together later. It's harder to break large commits up into smaller ones.

Smaller commits make git tools like `annotate` and `log` more useful. They also increase the chance that the commit can be useful on its own. This is frequently useful when you're working in parallel with another developer on a separate branch and you both need early access to the same work. It makes [cherry-picking](https://git-scm.com/docs/git-cherry-pick) much easier.

Pushes to master should be for absolute emergency [hotfixes](https://en.wikipedia.org/wiki/Hotfix) only, and with the agreement of one or more other members of the team.
