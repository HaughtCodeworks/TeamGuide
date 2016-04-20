# Code Review

Code reviews help all developers to better understand a project and the decisions that are made in the development process. When code reviews are a regular part of the developer workflow, there is always more than one person who is familiar with each part of the project. We are able to discuss our ideas and gain insight into different ways to approach a problem. As part of our [pull request process](/HaughtCodeworks/TeamGuide/blob/master/developer-workflow.md), the author of a branch tags 1-2 other developers to review her work and perform a code review.

## Notes for Everyone

* Accept that many programming decisions are opinions. Discuss tradeoffs, which you prefer, and reach a resolution quickly.
* Use PR comments to engage in respectful dialog regarding the code.
* Ask questions rather than make demands. ("What do you think about...")
* Ask for clarification.
* Avoid selective ownership of code. ("mine", "not mine", "yours")
* Be explicit. Remember people don't always understand your intentions online.
* Be humble. ("I'm not sure - let's look it up.")
* Don't use hyperbole ("always", "never", "endlessly", "nothing") or sarcasm.
* Talk in person if there is a misunderstanding or too many back and forth comments. Post a follow-up comment summarizing offline discussion.
* Consider and comment on style in code reviews. We prefer to draw our style inspiration from [GitHub's Style Guide](https://github.com/styleguide/ruby).

## Notes for the Author

* Keep in mind the review is of the code, not you.
* Thoughtfully consider the reviewer's suggestions and seek to understand their perspective.
* Explain why the code exists. ("It's like that because of these reasons. Would
  it be more clear if I rename this class/file/method/variable?")
* Extract some changes and refactorings into future tickets/stories if necessary.
* Push commits based on earlier rounds of feedback as isolated commits to the
  branch. Do not squash until the branch is ready to merge. Reviewers should be
  able to read individual updates based on their earlier feedback.
* Try to respond to every comment.
* Merge once reviewers have approved your PR, and you feel confident in the code and its impact on the project.

## Notes for the Reviewers

Understand why the change is necessary (fixes a bug, improves the user
experience, refactors the existing code). Then:

* Communicate which ideas you feel strongly about and those you don't.
* Identify ways to simplify the code while still solving the problem.
* Offer alternative implementations, but assume the author already considered
  them. ("What do you think about using...")
* Seek to understand the author's perspective.
* Sign off on the pull request  by approving it and giving a "Ready to merge" comment.