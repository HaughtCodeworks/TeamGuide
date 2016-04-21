# Developer Workflow

Each project may vary so this guide describes our standard workflow.

# Assigning Work

Each project will have a weekly planning meeting to go over what's new on the project, recently completed items, and what the team will work on in the coming week.  We cover the elements of this meeting in more detail in our [Project Planning Meeting guide](/project-planning.md).  We'll focus here on the developer-centric elements of work once it has been assigned.

# Card Review

During the planning meeting, the team will discuss with the client each item (which we refer to as a card) to be worked on.  Before we can proceed with any development we need to review each card, covering the card review elements below.  Our goal is to keep as much discussion as possible in the planning meeting, trying to avoid the need to have additional meetings, email exchanges or chat in order for a developer to start and complete work on the card.  Not every card will need this much discussion but consider each of these items and determine if it's appropriate to bring into the discussion.  Again, we don't want to waste time but we also want to avoid misunderstandings or miscommunication about what we need to do on the card.

## Card Review Elements

* Understand what the client is asking for.  The client should explain not only the business purpose of the change but any set expectations.
* What are the business requirements? Any existing specifications, technical requirements, mock-ups, or other supporting documents we should review?
* If the card represents a bug or defect, ask how it can be reproduced as well as the severity of the defect.
* Are there target dates either for initial review or going live with the change?  If so, find out more about the nature of those dates.  Are they fixed or flexible?  What's the consequence of missing the date?  Are they vital enough that the scope of the requested work should shift?
* Ask questions to clarify anything that you either don't understand or isn't clear in what has been covered so far.
* Explore edge case scenarios that may not have been covered to see how the client wants those resolved.
* If you are not 100% certain, clarify where in the application these changes should take place. For example, in more complex applications similar functionality may occur on different pages for different user types. If there's any ambiguity, make sure you clarify.
* Identify any related items that may match similar business functionality but may not have been mentioned explicitly by the client.
* Bring up any technical concerns with the requested change.  Making sure the client understands the costs and added complexity the card represents is crucial.  They will be making assumptions that things may be easier than they are and as developers we're often best equipped to highlight anything they may not be aware of.
* Clarify what exactly completion means for the card.  You will need this to determine when you're done and when the code makes whatever improvement or fix that the client needs.  This information will inform how you test and verify completion.
* Ask if the client has any related metrics that can indicate a positive business change in the card.
* Before you move on to the next card you should have enough information to do the following:
  1. Make a checklist of things you need to do to complete the card
  2. Map out your testing strategy to verify any change to the system

# Development

* Update the project board to indicate you've started on the card.
* Create a local feature branch in git based off master. Give your branch a short descriptive name based on the card on which you are working.
* Review the checklist and update it based on what you need to do for card completion.
* Map out your testing strategy for your card before you begin to change any code.  Refer to the [QA Mindset](/qa-mindset.md) document for guidance on the right level of testing.
* Consider breaking down the steps for completion into smaller chunks allowing you to test and commit those changes more quickly, especially if they are isolated in different parts of the system.  Update your checklist as appropriate.
* Work through each checklist item using test driven development to test, verify and complete that step.  Unless the step has no UI elements, manually test the change in the browser on your local environment.
* Consider whether refactoring the current step makes sense or if you should continue to the next checklist item.
* Once you've completed a step, make sure the entire test suite passes and your changes haven't broken the build.
* Verify your changes locally with real data. Play with the feature and ensure the user experience is good.
* Determine if this step should be committed on its own or if you want to include it in the next step.
* Add to the project README as you develop, making note of any steps required for deployment and testing: migrations, running scripts, updates to the server, etc. Add this information to your card, in addition to the README. See our [readme](/HaughtCodeworks/TeamGuide/blob/master/readme-guide.md) document for more on this.
* Stage your work into git verifying that all files necessary for this change are included and no unwanted changes or files will be committed.  Be extra careful that no files with sensitive data such as keys or passwords have been added.
* Commit to git, adding a meaningful message that describes the change from a business perspective and references the card ID.  It's important to note that these messages will most often be viewed by the team sometime in the future so make it useful from a historic and troubleshooting standpoint.
* Continue through the remaining checklist items on your card in the above manner until complete.
* When the entire card is complete, do a final review before moving to the team review process.
* Push your branch to origin.
* Submit a pull request on Github/BitBucket, and tag relevant reviewers from your team.
* Push your branch to the integration environment after verifying no one else on the team is using it. Verify that the functionality of your feature was properly deployed and works as expected.
* Update your card's status to indicate it's ready for team review.

# Team Review

* Post in team chat that your pull request is ready for review and your branch is on the integration environment.
* A team member other than the author reviews the pull request. Follow the [Code Review guidelines](/code-review.md) to avoid miscommunication. Make comments and ask questions directly on lines of code in the GitHub/ BitBucket repo or in team chat.
* Reviewers verify integration functionality before approving a pull request. Verification in integration should happen with a [QA mindset](/qa-mindset.md).
* Reviewers comment on any issues they see or any improvements that they feel are important enough to address before approving the PR.
* The author then addresses the feedback following the Development process above, introducing new commits as necessary.
* Reviewers and the author continue this process of review and feedback until the PR can be approved. Approval can be a formal approval, +1 or a comment such as 'Ready to merge' or 'Looks good'.
* Author of the PR reviews the branch's commits and determines any commits that need to be squashed through an interactive rebase.  Squash any meaningless commits such as the 'fixed whitespace' or 'missed this file' type so that all commits in the branch are valuable on their own with meaningful messages.
* Force push your branch, which will allow GitHub/ BitBucket to automatically close your PR once your commits are pushed to master.
* Pull master to make sure you're current.
* Merge your branch into master, ensuring that the merge message indicates the PR and card ID that the branch addresses.
* If any conflicts happen, address them and rerun your test suite to verify the resolution didn't break anything.
* Push master.
* Delete your remote feature branch.
* Delete your local feature branch.

# Deployment

* Once a pull request is approved and merged to master, master should be deployed to Staging.
* Perform any required steps for deployment outlined in the card. Double check that you've added these steps to the README so other team members know the steps to follow.
* Verify everything works as intended on Staging.
* Update the card on the planning board to indicate it's in Staging and ready to be reviewed by the client.
* Notify the team and client.
