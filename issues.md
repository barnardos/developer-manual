# Issues

We use [GitHub's issues](https://guides.github.com/features/issues/).

When creating a new issue, you should:

* create it in the appropriate repo
* apply one of the "type" labels
* place it into the "Product Team" project

If known at the time, you can also assign the appropriate people to the issue.

## How we write our issues

An issue is considered ready to be actioned when it has:

* a user story / job story
* acceptance criteria
* relevant links

These steps are covered in detail in our [team-handbook](https://barnardos.github.io/team-handbook/trello-cards).

## Making labels consistent across repos

You should update the labels when creating a new repo.

1.  Create the following `labels.json` file on your machine:

```json
[
  {
    "name": "estimate: 1",
    "color": "c5def5"
  },
  {
    "name": "estimate: 2",
    "color": "c5def5"
  },
  {
    "name": "estimate: 3",
    "color": "c5def5"
  },
  {
    "name": "estimate: 5",
    "color": "c5def5"
  },
  {
    "name": "estimate: 8",
    "color": "c5def5"
  },
  {
    "name": "estimate: 13",
    "color": "c5def5"
  },
  {
    "name": "status: blocked",
    "color": "f9d0c4"
  },
  {
    "name": "status: blocker",
    "color": "d4c5f9"
  },
  {
    "name": "type: bug",
    "color": "ee0701"
  },
  {
    "name": "type: chore",
    "color": "5551A8"
  },
  {
    "name": "type: refactor",
    "color": "1d76db"
  },
  {
    "name": "type: research",
    "color": "CA2BAF"
  },
  {
    "name": "type: spike",
    "color": "006b75"
  },
  {
    "name": "type: story",
    "color": "0e8a16"
  }
]
```

2.  Create a [GitHub access token](https://github.com/settings/tokens).
3.  Do a dry-run using `npx github-label-sync --access-token xxxxxx --labels labels.json --dry-run barnardos/yyyyyy` but:
    * replace `xxxxxx` with your access token
    * replace `yyyyyy` with the repo name
    * ensure `label.json` points to the file you created
4.  If the dry-run looks good, run the command again without the `--dry-run` flag.
