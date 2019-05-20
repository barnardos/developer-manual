### Reviewing Dependabot's Pull Requests

- Check that the review app on heroku works if there is one (We don't always have them so you might have to pull the branch and check it out locally on your machine)
- Rebase if needed - you might be lucky enough to be up to date!
To do this you can comment ```@dependabot rebase``` on the PR and Dependabot will do it for you and 'like' your comment to confirm that the instruction has been received.
- check the PR comment made by dependabot which should contain all the info about commits made and any new entries in the changelog which may have implications for your code 
- Look at the code diff to see what changes have been made - maybe the dependencies on that dependencies may effect something else in your system unrelated to the gem which is being updated
- security PRs take precedence over other PRs
- Different languages should be dealt with by the appropriate developer i.e. JS -> FE, Ruby -> BE

