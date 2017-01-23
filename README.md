![welcome-teal](https://cloud.githubusercontent.com/assets/194400/22215755/76cb4dbc-e194-11e6-95ed-7def95e68f14.png)

Firstly, a ***heartfelt thank you*** for
making time to contribute to this project! <br />
As a _distributed_ team we _rely_ on the contributing guide steps
to keep our communication clear. <br />
_Please_ let us know if anything is _unclear_
or if you have any suggestions
for how to simplify things.

## _New_ To The Project?

### Step 1: Check if the Idea/Story/Issue _Already Exists_ Using GitHub  ![search](https://cloud.githubusercontent.com/assets/194400/22224334/255930a8-e1b6-11e6-9953-12cd4739aa1c.png)

1. Please take a minute to **read through the existing stories/issues**
for the project to familiarize yourself with the current "backlog".

1. Try **searching** through the existing issues for _keywords_ associated
with the story/issue you want to create, <br />
e.g: https://github.com/dwyl/time/issues?utf8=%E2%9C%93&q=is%3Aissue%20app+icon
if `email` was your keyword.

1. Otherwise, if you are (_reasonably_) sure there is no _existing_ issue/story
covering what you have in mind, create a new issue (_see next step_!)


### Step 2. Create a New User Story _or_ Report an Issue ![New Issue](https://cloud.githubusercontent.com/assets/194400/22224203/bbc5efb4-e1b5-11e6-9fcb-3aae75ae74ed.png)

1. Using the `New Issue` button, create an issue for the user story or issue

  + A good user story describes the problem in a concise user-focussed way:
  Example user story:
  ```
  As a person using the app
  I want to be able to save my preferences for content
  so that I can see content that is relevant to me when I open the app.
  ```
  or if you are reporting an issue/bug/fault try and include
  the exact steps to "_reproduce_" the issue. example:
  ```
  when using the app on
  ```
  + Please *include* as much ***relevant information*** as you can
  so the Product Owner (_or project leader_) can decide if
  it is a necessary/desired feature.
  Example of useful details:
  ```
  People using the app will only access the app from their company-issued
  Android (Lollipop) Mobile phone (5 inch Samsung Galaxy J)
  The screen resolution of 1080 x 1920 pixels
  ```
  or
  ```
  People use the app in areas with poor mobile signal
  so the app has to work offline and sync data/changes later when on wifi.
  ```
  or for a when reporting an issue (_potential bug_):
  ```
  People using Windows 8 and Internet Explorer 10 report that
  they cannot click on the button to save their settings.
  ```
+ **Before beginning any work**, await confirmation of the need for the user
story from the Product owner (or Project Maintainer).
+ That's it! You don't need to do anything else until the need is confirmed and prioritized. You can check back later to see if this has happened.

Verify the Need/Issue


> **Note**: if you have a security/privacy related question that you want
to ask or disclose privately, please email us: [hello+security@dwyl.io](mailto:hello+security@dwyl.io)

<br />

## Existing Team Members

### 3. After need is confirmed

1. The person acknowledging the user story will typically add some labels to
the issue, but you can still add [any other relevant
 labels](https://github.com/dwyl/labels/labels) eg. `question`
, `discuss`, etc.
+ Product owner (or Project Maintainer) will add a priority label to the issue
 (**_1-5_**)
+ _Where needed_, split the user story into individual technical tasks (not
  required for a single task/small user story)
+ Add an estimated time label for each task (**_documentation + development +
  tests + styling (if applicable)_**)
+ Add a time estimate to the _user story_ (derived from technical tasks)


_Note:_ For work in sprints, a **milestone** is added **at the sprint planning
session** to group the user story with its relevant sprint.

### 4. Work on the Technical Tasks

1. Assign the technical task to yourself
2. Add the `in-progress` label to the task so that your team knows it is currently being worked on and when it began
3. Update the `README.md` before working on a task: **what, why, how**
4. [Add comments to the issue as you work](https://github.com/dwyl/learn-nightwatch/issues/8) to update your team of your progress and any sticking points you might experience along the way (**_this allows people to help you more effectively and gives your client something measurable_**)
  + If you haven't finished your current task by the end of the day, take 10 minutes to describe the progress you've made and what else needs doing - anyone should be able to pick up and complete a user story by reading this description
+ **Every commit you make should reference a user story or technical task**
+ Once you've made a commit, push up your changes and then open a PR _(even if the work isn't yet finished)_ so that the rest of your team can easily see what you've been working on
  + Add `[WiP]` before the title of your PR and add that it's **NOT READY FOR REVIEW** in the description if it's still in progress

#### 4. Complete the Task

1. Make sure all tests are passing and that your code coverage is ✅ 100%
+ Increment the version of your application
+ Remove the `[WiP]` from your PR title and change the description to **READY FOR REVIEW**
+ Make sure your pull request is [ready for review](#pull-requests)
+ Assign someone to review your pull request
+ Delete the `in-progress` label and _add an `in-review` label_
+ Update the time label if necessary

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

+ **When you submit your pull request, include:**
  + A **descriptive title** that answers the question "What does this PR do?"
  + A reference to the issue that the PR solves
  + An explanation of what the PR includes (**bullet pointed lists** are sometimes helpful to make things clearer) and the _implementation detail_
  + An **update to the documentation** (often the repo's readme)
  + Make sure your PR **adds tests** for the new code you have written
  + If you have the permissions to do so, **assign your pull request** to someone for review (this person will be the first point of contact if the PR merges a bug into the production environment)

A good example is this one: https://github.com/indexzero/ps-tree/pull/12 ((created from the need which was confirmed in [this issue](https://github.com/indexzero/ps-tree/issues/10))).

#### Images and Binary Files

When making a pull request, make sure that you haven't included any ***unnecessary*** files that will take up a lot of space.  
Such files include images and other binary type files.  
Git is meant for source code and other (text-based) files that require version control.
Images and other binary files are difficult for a human to review in a GitHub Pull Request.
This means that when ever a person clones/pulls the code they have to _download_ many/huge files (_not just the code which is typically tiny by comparison_)
> It is a _general_ `git` "_best practice_" to avoid _clogging_ up your Git repo with files that don't need to be under version control.


### Stars 🌟 (share the love!)

***After you've contributed to one of our repos, or if you've found one of them helpful or useful in any way, please share the love by starring it.
This shows other members in the developer community that it's a worthwhile project or learning resource and one that can offer value to other developers like you!*** 🌟



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

## *What?*

### Issues

At dwyl we use _issues_ to log our user stories and technical tasks to ensure we have a [single version of the truth](https://github.com/dwyl/github-reference#why).  
User stories describe features of the application in terms of their value to the *user*.

### Issues > Validation

This may feel a bit "_bureaucratic_" but (_we find that on balance_) it makes for better remote working because less discussion is "lost" and means everyone can follow along regardless of their location.

## Additional Information

We are releasing our work under the GNU General Public License Version 2 (GPL V.2)
if you have any questions regarding the license, please read:
https://github.com/dwyl/intellectual-property and raise an
[issue](https://github.com/dwyl/intellectual-property/issues)
on GitHub if you require clarification!
