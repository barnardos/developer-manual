### Configuring Dependabot on a new project

*Sign in Barnardo's Github account* (barnardos-admin), password in 1Password.

Go to [https://app.dependabot.com/accounts/barnardos/](https://app.dependabot.com/accounts/barnardos/)

Click on Add repos.

Click on grant access to additional repos if the repo isn't in the list, otherwise select it from the list along with the language you want dependabot to manage (more can be added later).

The repo should now be in the list on [https://app.dependabot.com/accounts/barnardos/](https://app.dependabot.com/accounts/barnardos/)

Click on the settings cog to check them, usually the default one should be fine but double check that:

* Daily updates
* Directory is `/`
* Only top-level dependencies (and security patches for subdependencies)
* Update strategy is set to Auto
* Automatic PR merging dropdowns are both set to None

If you want to dependabot to automatically assign reviewer(s) and assignee(s) to Dependabot's PR, make sure you use their Github name without the @.
