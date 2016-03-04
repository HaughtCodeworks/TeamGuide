# Project Management Boards

Our team uses project boards to manage our projects and track our progress.  The boards serve two purposes: to allow clients to see what's happening and give feedback on a project, and to allow us to manage our team, our tasks, and stay coordinated. Each project has its own board. The board shows us the current state of all the things we're working on in our project and where each task is in the lifecycle of development. Each task is represented by a card on the board, and as cards move through the development process, we move them to different columns on the board.

Everything the team is working on for a project, whether a feature, a bug, or a chore, should be represented by a card. We can't track something if it's not on the board. If we're doing something that's not represented by a card, we should ask why.

## Board Flow

Our current project board tool is not very expressive in some ways, and this leads us to add additional columns to our board. Currently, we have a "Backlog" column in our project board. Once Feature Complete is up and running, our backlog will live in the Features area of the app rather than on the project board itself. The "Backlog" column is where we store tasks that will need to be completed but it's either not the right time to begin work on them or they haven't yet been approved.

#### The "Next" Column
Once cards are approved and ready for developers to begin working on them, we move them to the "Next" column. Cards in this column are our queue of work, and are waiting for someone to be assigned to them. A developer can assign themselves to a card when they are ready to begin work on it.

#### The "Development" Column

The "Development" column is for cards that are actively being worked on. It is important that a developer has only one card in this column at a time. If they need to work on something else, this card can move back to ready so as not to let things build up or block. Our project board system follows the traditional Kanban pull based system pretty closely. Things can only move right if there's space for them, and a dev team can really only take on 3-4 cards at once in the development stage. More than that and things sit idle. The board should be an accurate reflection of the project at any point in time, so if a developer is not currently working on a card in the "Development" column, they can move it back so our progress is accurately reflected.

#### The "Needs Review" Column

When a developer has completed the task on a card, we kick off the (pull request process)[https://github.com/HaughtCodeworks/TeamGuide]. The "Needs Review" column represents cards currently under code review in the PR process. After a PR has been fully approved, the feature is merged into the master branch and deployed to the staging environment.

#### The "Staging" Column

Cards in the "Staging" column are ready for client review on the staging environment. The client makes sure everything on the feature works as expected.

#### The "Approved" Column

Once clients have tried out a feature and approved a card in "Staging", they move the card to the "Approved" column.

#### The "Live" Column

After the client moves a card to "Approved", a developer will deploy the app to the live environment. We verify it internally, and the client needs to approve and sign off on the feature. At this point, the task card is considered complete. We close the task card, and move it from the board.

## Cards

Cards each represent a specific component of a project, such as a user story, bug fix, development or design task, or a general to-do. The tasks on a card should match an ideal pull request size so that the card can follow a pull request as it goes through. A card that includes too many tasks would lead to multiple pull requests on the same card. If you find this is the case, split a task into multiple cards.

#### Card Components

* Card Title: The title of a card should be a short descriptive phrase or sentence (1-2 lines) that identifies it from other cards at a glance, and makes sense to the client and to the dev team.

* Card Description: The description is where we capture the summary of requirements, bug details (how to reproduce), and all the details we need to know that couldn't go in the title.

* Card Checklist: The checklist is created by the developer doing the work on the card. It is not a required step, but can be useful to help break down and identify everything important to do or verify. The checklist is the developer's understanding of actionable items coming out of the description. This allows the developer to remember everything, and makes it easy for others to see how the task is progressing.

* Card Comments: Comments are valuable because they allow a conversation to happen that can be referenced and they allow communication specific to the card that we want to reference. A member of the project board can choose to be notified that someone is leaving comments. Usually the client gets involved in comments, and it is nice to be able to track the comments back and forth.

* Card Members: A member of the board can assign themselves or another developer to a card. We use it as a way to know who is responsible or actively on the card.

* Card Labels: Labels are useful for identifying something about the card that you want to draw attention to. We use them to represent additional things that need to be done on a feature, such as migrations or data scripts, etc.

* Card Attachments: It is sometimes important for files to be part of the task at hand. Usually the client is the one adding attachments to a card. In general we like to use Dropbox, but sometimes screenshots, etc. are nice to have on the card itself.
