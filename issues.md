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

Here is [an example of a well written issue](https://github.com/barnardos/design-system/issues/118).

## Making labels consistent across repos

You should update the labels when creating a new repo.

1.  Create the following `labels.json` file on your machine:

```json
[
  {
    "name": "BE",
    "color": "837ccc"
  },
  {
    "name": "FE",
    "color": "f99dc7"
  },
  {
    "name": "UX",
    "color": "d6b833"
  },
  {
    "name": "Blocked",
    "color": "f9d0c4"
  },
  {
    "name": "Blocker",
    "color": "d4c5f9"
  },
  {
    "name": "Bug",
    "color": "ee0701"
  },
  {
    "name": "Chore",
    "color": "5551A8"
  },
  {
    "name": "Refactor",
    "color": "1d76db"
  },
  {
    "name": "Research",
    "color": "CA2BAF"
  },
  {
    "name": "Spike",
    "color": "006b75"
  },
  {
    "name": "Story",
    "color": "0e8a16"
  }
]

```

2.  Click on `Generate new token` here: https://github.com/settings/tokens. Add a token description and tick repo (which will tick four boxes for you). This will generate an access token, take a note of it in 1password as you will only be able to see it once.
3.  Do a dry-run using `npx github-label-sync --access-token xxxxxx --labels labels.json --dry-run barnardos/yyyyyy` but:
    * replace `xxxxxx` with your access token
    * replace `yyyyyy` with the repo name
    * ensure `label.json` points to the file you created
4.  If the dry-run looks good, run the command again without the `--dry-run` flag.
