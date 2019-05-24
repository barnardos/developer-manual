### Reviewing Dependabot's Pull Requests

- Check that the review app on heroku works if there is one. 
- If there's no heroku review app pull the branch and check it locally on your machine.
- Rebase if needed. 
To do this comment `@dependabot rebase` on the PR and Dependabot will do it for you and 'like' your comment to confirm that the instruction has been received.
- Look at the code diff to see what changes have been made.
(The dependencies on that dependencies may effect something else in your system unrelated to the gem which is being updated).
- Check the PR comment made by dependabot.
It should contain all the infos about commits made and any new entries in the changelog which may have implications for your code.
- Security PRs take precedence over other PRs.
- Different languages should be dealt with by the appropriate developer i.e. JS -> FE, Ruby -> BE.

