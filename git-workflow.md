# Git Workflow

At Haught Code Works, we use a rebase-centered git workflow. This helps us avoid uninformative merge commits and gives us a more verbose git history. We work on feature branches and rebase interactively onto master when we're ready to commit. We rebase interactively so we are able to modify our commits as needed by rephrasing commit messages or squashing related commits. The following is an overview of our git workflow.

* A developer creates the central git repository for a project (git init)
* Other developers on the project clone the central repository (git clone repo-name)
* As developers assign themselves to cards on our (project board)[], they start their work on a local feature branch, which is given a short name based on the project board card title (git checkout -b branch-name)
* When developers finish work on a feature branch, they push the local branch to the remote repo, create a pull request, and go through the code review process.  When pushing a branch to origin for the first time, we use the "-u" flag so we have an upstream tracking reference for the branch.


* Rebase vs. merge: git pull --rebase
* Interactive: opens the editor and lets you enter commands for the commits to be rebased. This lets you manage the git history.
* git commit --amend: lets you fix the most recent commit. You can combine new changes with the prior commit instead of doing a new commit, or you can edit the commit message. It replaces the most recent commit, so should not be done on work that others are using.
* git cherry-pick: lets you merge a commit from one branch into another. This is useful when a merge of the full feature branch is not useful or is incompatible.
* Past tense commit messages-- ask about the lengthy commit message on Thoughtbot. Don't use -m?  Answer the 4 questions?
* PR and code reviews

http://scottchacon.com/2011/08/31/github-flow.html
http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
