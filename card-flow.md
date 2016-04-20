# Project Management Boards

Our team uses a web-based Kanban planning tool, such as Trello or AgileZen, to manage our projects and track our progress. The boards serve two purposes: to allow clients to see what's happening and give feedback on a project, and to allow us to manage our team, our tasks, and stay coordinated. Each project has its own board. The board shows us the current state of all the things we're working on in our project and where each task is in the lifecycle of development. Each task is represented by a card on the board, and as cards move through the development process, we move them to different columns on the board.

Everything the team is working on for a project, whether a feature, a bug, or a chore, should be represented by a card. We can't track something if it's not on the board. If we're doing something that's not represented by a card, we should ask why.

## Board Flow

In Kanban, we add cards on the far left-most column that are to be worked on by the team. As cards are ready to be worked on and there's availability by the team, we move the cards to the right as they go through the steps of software development.  Each column represents the stages that a specific project has defined.  We will illustrate our common flow below but each project may modify this based on business conditions.

### Where's the backlog or icebox columns?

Some tools have a place to keep cards that don't 'fit' into the current iteration or cycle of work.  This concept doesn't exist in Kanban and it's been our experience that trying to mimic either backlogs or iceboxes lead to out-dated and wasteful cards that ultimately slow down the team.  Instead we have the client keep any extra work not quite ready to be tackled elsewhere.  This allows only 'fresh' ideas to enter the board to be worked on by the team in the next 1-2 weeks at most.

### The "Next" Column
Once cards are approved and ready for developers to begin working on them, we move them to the "Next" column. Cards in this column are our queue of work, and are waiting for someone to be assigned to them. A developer can assign themselves to a card when they are ready to begin work on it.

### The "Development" Column

The "Development" column is for cards that are actively being worked on. It is important that a developer has only one card in this column at a time. If they need to work on something else, this card can move back to "Next" so as not to let things build up or block. Our project board system follows the traditional Kanban pull based system pretty closely. Things can only move right if there's space for them, and a dev team can really only take on 3-4 cards at once in the development stage. More than that and things sit idle. The board should be an accurate reflection of the project at any point in time, so if a developer is not currently working on a card in the "Development" column, they can move it back so our progress is accurately reflected.

### The "Needs Review" Column

When a developer has completed the task on a card, we kick off the pull request process, which is explained in more detail in our [developer workflow](/HaughtCodeworks/TeamGuide/blob/master/developer-workflow.md) document. The "Needs Review" column represents cards currently under code review in the PR process. After a PR has been fully approved, the feature is merged into the master branch and deployed to the staging environment.

### The "Staging" Column

Cards in the "Staging" column are ready for client review on the staging environment. The client makes sure everything on the feature works as expected.

### The "Approved" Column

Once clients have tried out a feature and approved a card in "Staging", they move the card to the "Approved" column. Cards in this column are ready to be promoted to production. Each project will have its own rules on when we deploy to production so make sure these get scheduled and communicated with the client and team before they're deployed.

### The "Live" Column

Once a card has been deployed to the production environment, the team will verify it internally to make sure it was successfully deployed. Once that is done the client should be notified so they can review and approve the card. This is the final step in the lifecycle, so archiving a card out of "Live" should be done by the client to indicate that they accept this change as complete.

## Cards

Cards represent a request for work such as a new feature, a user story, bug fix, design modification or anything else that the team needs to perform while having its progress tracked by the client.
A single card should contain a reasonable size of work that should be completed and shipped together. Though we may break down a card into tasks via a checklist, ideally all should fit into a single pull request and move across the board as one. A card that includes too many tasks would lead to multiple pull requests on the same card. If you find this is the case, split a task into multiple cards.

### Card Components

* Card Title: The title of a card should be a short descriptive phrase or sentence (1-2 lines) that identifies it from other cards at a glance, and makes sense to the client and to the dev team.

* Card Description: The description is where we capture the summary of requirements, bug details (how to reproduce), and all the details we need to know that couldn't go in the title.

* Card Checklist: The checklist is created by the developer doing the work on the card. It is not a required step, but can be useful to help break down and identify everything important to do or verify. The checklist is the developer's understanding of actionable items coming out of the description. This allows the developer to remember everything, and makes it easy for others to see how the task is progressing.

* Card Comments: Comments are valuable because they allow a conversation to happen that can be referenced and they allow communication specific to the card that we want to reference. A member of the project board can choose to be notified that someone is leaving comments. Usually the client gets involved in comments, and it is nice to be able to track the comments back and forth.

* Card Members: A member of the board can assign themselves or another developer to a card. We use it as a way to know who is responsible or actively on the card.

* Card Labels: Labels are useful for identifying something about the card that you want to draw attention to. We use them to represent additional things that need to be done on a feature, such as migrations or data scripts, etc.

* Card Attachments: It is sometimes important for files to be part of the task at hand. Usually the client is the one adding attachments to a card. In general we like to use Dropbox, but sometimes screenshots, etc. are nice to have on the card itself.
