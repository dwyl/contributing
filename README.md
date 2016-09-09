# contributing

Guidelines for people contributing to dwyl projects

Firstly, a ***heartfelt thankyou*** for even *considering* contributing to the dwyl project!
We rely on contributions from *many* ***fantastic people*** to make dwyl a reality
and are *excited* that you are reading this in order to join the fun!

We (dwyl) are building our company using the open source code others have published
and consequently we think its *only fair* that everything we make is also open source.

We are releasing our work under the GNU General Public License Version 2 (GPL V.2)
if you have any questions regarding the license, please read:
https://github.com/dwyl/intellectual-property and raise an
[issue](https://github.com/dwyl/intellectual-property/issues)
on GitHub if you require clarification!

See: https://github.com/dwyl/contributing/issues/1 + https://github.com/dwyl/summer-2015/issues/27

## Recommended Guidelines

### Workflow

Before you begin any work on a dwyl project please open an issue on the repository that you wish to contribute to.

There **_must_** be a **comment** from **at least one other person** on the issue acknowledging it and/or confirming the requirement/bug before work starts. This is necessary to avoid doing _unnecessary work_. e.g. someone may have already solved that problem or implemented a similar feature on a different project and can point you in the direction of sample code or the PO/Client may deem the issue/story to be lower priority than something else on the list. The recommended workflow is as follows:

1. First read through the existing stories/issues for the project to familiarise yourself with the current "backlog".
2. Think of the keywords associated with the story/issue you want to create.
3. Perform a quick search through the existing issues for the project with the keywords you identified e.g: https://github.com/dwyl/time/issues?utf8=%E2%9C%93&q=is%3Aissue%20email if email was your keyword.
4. Once you are (quite) sure there is no existing issue/story covering what you want to solve/create, move on to [creating one](#create-the-user-story-and-its-technical-tasks)

### Issues

At dwyl we use _issues_ to log our user stories and technical tasks for a given project. User stories are higher level issues that describe certain functionalities of the application you're building. These user stories get broken down into smaller **_technical_** tasks.

### Issues > Validation

After creating an issue/story (_before you estimate the time required or start working on it_) get people's input/feedback to _confirm_ that the description of the story is clear, has enough detail and addresses a real need/issue.

This may feel a bit "_bureaucratic_" but (_we find that on balance_) it makes for better remote working because less discussion is "lost" and means everyone can follow along regardless of their location. See our [workflow](#workflow) above!

Here is our step-by-step process for creating and developing a user story and its technical tasks:

Example user story: `As an admin I want to be able to create new users because I don't want unknown users to be able to use my application`

#### Create the User Story and its Technical Tasks
1. Create an issue for each of your user stories
2. Add an estimated time label for each
3. Add a milestone to group the user story with its relevant sprint
4. Split the user story into individual technical tasks
5. Add an estimated time label for each task (**_documentation + development + tests_**)
4. Add a priority label to each technical task (**_1-5_**)
5. Add descriptive labels that describe the task in more detail

#### Begin Work on the Technical Tasks
1. Assign the technical task to someone on your team (_or yourself_)
2. Add the 'in-progress' label to the task so that your team knows it is currently being worked on and when it began
3. Update the `README.md` before working on a task: **what, why, how**
4. Add comments to the technical task to update your team of your progress and any sticking points you might experience along the way (**_this allows people to help you more effectively and gives your client something measurable_**)
5. Periodically check GitHub notifications to see if someone has responded to your comments
6. If you haven't finished your current task by the end of the day take 1/2h to describe the progress you've made and what else needs doing. Anyone should be able to pick up and complete a user story by reading this description
7. Every commit you make should reference a user story or technical task
8. Once you've made a commit, push up your changes and then open a PR so that the rest of your team can easily see what you've been working on. Add `[WiP]` before the title of your PR and add that it's **NOT READY FOR REVIEW** in the description.

#### Complete the Task
1. Make sure all tests are passing and that your code coverage is ✅ 100%
2. Increment the version of your application
3. Remove the `[WiP]` from your PR title and change the description to **READY FOR REVIEW**
4. Assign someone to review your pull request
5. Delete the 'in-progress' label
6. Update the time label if neccessary
7. Close the user story referencing the PR

_These guidelines for creating user stories are an adaptation of [Simon's](https://github.com/simonlab) [**user-story-checklist**](https://github.com/SimonLab/user-story-checklist) repo. Check it out!_

### Pull Requests

At dwyl we like to work in the most ***agile*** way possible.
This extends to how we submit and review our **pull requests**.

> **Rule**: _**One thing** (feature or bug fix) **per pull request**_.

You might be _tempted_, to bundle up _several_ bug fixes/feature additions into
one _large_ PR and then submit it to be reviewed all at once.
We prefer working in _smaller increments_ splitting the work
into individual parts to be reviewed separately. The reasons are:

+ It allows us to keep track of the work more easily because it provides more
_descriptive_ reference points
("[_paper trail_](https://en.wiktionary.org/wiki/paper_trail)")
to which we can look back at in future if required
+ It gives the person reviewing the PR a single focus for the change/bug-fix
which improves review speed.

> Further reading: "Working in Small Batches":  http://www.startuplessonslearned.com/2009/02/work-in-small-batches.html

### Labels

GitHub can be a _great_ project management tool if used _effectively_. One of the ways you can manage your project backlog is through **labels**. Labels are a great way to **organise** and **track** the progress of a given project at _any_ point in time. [Here's why we choose to use GitHub](https://github.com/dwyl/github-reference#why)

At dwyl we have created our _own_ standard list of labels that we use for each of our projects. This gives our developers the ability to move between projects **quickly** and **productively**, saving time and energy in the process.

Here is our **[complete list](https://github.com/dwyl/contributing/labels)** of labels and how they should be used:

![labels](https://cloud.githubusercontent.com/assets/12450298/18248682/afcd6974-7371-11e6-84bf-0cb9f4677d92.png)

Github gives you a pre-populated list of labels for you to use. They are:

- `bug` #EE0701 - report a bug that needs fixed
- `duplicate` #CCCCCC - duplicate issue
- `enhancement` #84B6EB - improving existing code
- `help-wanted` #128A0C - looking for help or expertise on a subject
- `invalid` #E6E6E6 - GitHub standard tag (not used)
- `question` #CC317C - for open questions and discussions
- `wontfix` #ffffff - when an issue won't be addressed (with reason why in comment)

Here are the custom ones that we use at dwyl:

- `in-progress` #009688 - to be added when an issue has been assigned
- `in-review` #128A0C - once a PR has been submitted relating to the issue
- `please-test` #08E700 - added after PR is merged (assign to product owner)
- `priority-1` #0D47A1 - drop everything and work on this (used only when _completely_ neccessary)
- `priority-2` #1976D2 - high priority issue (what needs doing now)
- `priority-3` #42A5F5 - high priority (what needs doing next)
- `priority-4` #8DC9F9 - low priority (to be upgraded later)
- `priority-5` #C5DEF5 - lowest priority (non-urgent changes)
- `T[x]d` #F06292 - time in 'x' days it should take (estimation)
- `T[x]h` #F7C6C7 - time in 'x' hours it should take (estimation)
- `technical` #D4C5F9 - technical issue for developers
