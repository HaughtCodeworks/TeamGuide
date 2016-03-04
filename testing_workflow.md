# Testing Workflow

We rely on feedback from each other to improve the quality of our code. Our process for workflow and pull requests as written below is inspired by Thoughtbot's playbook, as is the related section on Code Review. We'd like to credit Thoughtbot and thank them for sharing their playbook.

## Workflow Steps

* Create a local feature branch based off master. Give your branch a short descriptive name based on the card on which you are working.
* When your feature is complete, verify it works locally and all tests pass.
* Consider if you need to break your changes into multiple commits. Once you've grouped your changes into logical commits, add a good commit message. Make sure that you are only committing the changes that make sense for this feature.
* Push your branch to origin, and avoid including sensitive files in source control.
* Submit a pull request on Github/BitBucket, and tag relevant reviewers from your team.

### Pull Request Process

* Post in Hipchat that your PR is ready for review.
* A team member other than the author reviews the pull request. Follow the Code Review guidelines (see related document) to avoid miscommunication. Make comments and ask questions directly on lines of code in the GitHub/ BitBucket repo or in Hipchat.
* When satisfied, the reviewer approves and comments on the pull request “Ready to merge" or "+1”.
* The author of the PR rebases interactively. Squash commits like “Fix whitespace” into one or a small number of valuable commit(s). Edit commit messages to reveal intent. Run tests.
* View a list of new commits and view changed files. Merge your branch into master.
* Force push your branch, which will allow GitHub/ BitBucket to automatically close your PR once your commits are pushed to master.
* Push to master.
* Delete your remote feature branch.
* Delete your local feature branch.

### Deploying

Deploy to dev/integration. The author of the pull request verifies, and has another engineer verify as well, before something is completed. Verification in integration should happen with a QA mindset. Once verification in integration is complete, send to staging for client approval.

