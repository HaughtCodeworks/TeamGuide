# Developer Workflow

We rely on feedback from each other to improve the quality of our code. Feedback is important at all levels of what we do. Our developer workflow allows us to work on our own, yet leverage meaningful feedback without taking too much time away from the rest of the team. Our workflow allows the whole team to be aware of what's happening and changing on the project. In our pull request process and [code reviews][/HaughtCodeworks/TeamGuide/blob/master/code-review.md], we check on code quality and benefit from the team's expertise and project know-how without constantly pairing.

## Development Steps

* Claim a card from the project board. For more details on this step, visit our [card flow](/HaughtCodeworks/TeamGuide/blob/master/card-flow.md) document.
* Identify what needs to be done to complete this card. What does it mean for a feature to be complete? (create and reference separate post on this)
* Create a local feature branch based off master. Give your branch a short descriptive name based on the card on which you are working.
* Determine an appropriate level of testing for your branch, and decide how you will test your work. (create and reference separate post on testing)
* When you are finished with your feature, make sure the entire test suite passes and your work hasn't broken the build.
* Verify everything works locally with real data. Play with the feature and ensure the user experience is good.
* Add to the README as you develop, making note of any steps required for deployment and testing: migrations, running scripts, updates to the server, etc. Add this information to your card, in addition to the README. See our [readme](/HaughtCodeworks/TeamGuide/blob/master/readme-guide.md) document for more on this.
* Consider if you need to break your changes into multiple commits. Once you've grouped your changes into logical commits, add a good commit message. Make sure that you are only committing the changes that make sense for this feature.
* Push your branch to origin, and avoid including sensitive files in source control.
* Submit a pull request on Github/BitBucket, and tag relevant reviewers from your team.
* Push your branch to the integration environment after verifying no one else on the team is using it. Test the functionality of your feature on integration to make sure it works.
* Move your card on the planning board to the "In Review" column.

### Pull Request Process

* Post in team chat that your pull request is ready for review and your branch is on the integration environment.
* A team member other than the author reviews the pull request. Follow the [Code Review guidelines](/HaughtCodeworks/TeamGuide/blob/master/code-review.md) to avoid miscommunication. Make comments and ask questions directly on lines of code in the GitHub/ BitBucket repo or in team chat.
* Reviewers verify integration functionality before approving a pull request. Verification in integration should happen with a [QA mindset](/HaughtCodeworks/TeamGuide).
* When satisfied, the reviewer approves and comments on the pull request “Ready to merge" or "+1”.
* The author of the PR rebases interactively. Squash commits like “Fix whitespace” into one or a small number of valuable commit(s). Edit commit messages to reveal intent.
* View a list of new commits and view changed files.
* Run the test suite.
* Force push your branch, which will allow GitHub/ BitBucket to automatically close your PR once your commits are pushed to master.
* Merge your branch into master and push master.
* Delete your remote feature branch.
* Delete your local feature branch.

### Staging your Changes

* Once a pull request is approved and merged to master, master should be deployed to staging.
* Perform any required steps for deployment outlined in the card. Double check that you've added these steps to the README so other team members know the steps to follow.
* Verify everything works as intended.
* Update the planning board by moving the card to "Staging". At this point, you indicate the code is ready to be reviewed by the client.
* Notify the client.

