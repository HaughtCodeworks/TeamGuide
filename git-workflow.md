# Git Workflow

At Haught Codeworks, we use a rebase-centered git workflow. This gives us a more verbose git history and helps us avoid uninformative merge commits. We work on feature branches and rebase interactively onto master when we're ready to commit. We rebase interactively so we are able to modify our commits as needed by rephrasing commit messages or squashing related commits.

## Maintaining a Repository and Working on Branches

* A developer creates the central git repository for a project
* Other developers on the project clone the central repository: `git clone repo-name`
* Before starting work on a new feature, the developer makes sure master is up to date on their local machine: `git fetch origin`  `git rebase origin/master`
* The developer assigns herself to a [card](/card-flow.md) on our project board, and starts her work on a local feature branch, which is given a short name based on the project board card title: `git checkout -b branch-name`
* As developers work, they make sure not to include files with sensitive information or files specific to local development in version control.
* When a developer finishes work on a feature branch, they follow the steps below to push their local work to the remote.

## Pushing a Branch to Remote

  * Add files to the staging area: `git add`
  * Commit your work. Squash unneeded commits such as "Fixed white space." If you need to revise a commit message, or add to a commit that has not yet been pushed to the remote repository, use `git commit --amend`.Commit staged files with a concise yet informative commit message (`git commit -m "Added all team members to authors.yml with original bios"`).
  * Push the local branch to the remote repository. When pushing a branch to origin for the first time, we use the "-u" flag so we have an upstream tracking reference for the branch: `git push -u origin branch-name`
  * Create a pull request, and go through the [code review](/code-review.md) process
  * Once the code review process is complete, and the branch is approved, it can be merged into master.

  ## Merging with Master

* From the feature branch on your local machine, rebase master interactively: `git rebase -i master`
* Force push your feature branch so GitHub/ Bitbucket marks it as merged: `git push branch-name -f`
* Switch to master and merge your branch: `git merge branch-name`
* Push master to the remote repository: `git push origin master`
* Once you have merged and pushed to master, delete your local and remote feature branch.