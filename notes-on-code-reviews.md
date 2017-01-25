# Notes on code reviewing

> "*Programs are meant to be read by humans,  
> and only incidentally for computers to execute*." - Donald Knuth
- - -

> “*Any fool can write code that a computer can understand.  
> Good programmers write code that humans can understand*.”
> ~ Martin Fowler
- - -

![code quality cartoon](http://i.imgur.com/IC3cJde.png "code quality cartoon")

Our goal is *zero* surprises ("WTF" moments) during code review.

## Why review code?

Reading other people's code is the ***fastest way to learn***,
not only do you gain insight into how other people solve a problem,
you also gain experience in what makes code ***readable*** (*and thus* ***maintainable***).

While it may *feel* like the focus of your first 8 weeks of Founders &
Coders is on learning to *write* code, as a coder you will spend *considerably* more time *reading* other people's code than writing your own. (*get used to that idea... embrace it! if you can write less code by reading other people's modules and using existing solutions, you save everyone time!*)

In many cases the **cost** of ***maintaining*** **software** ***can vastly exceed*** the **initial cost** of **development**.

![Software Life-Cycle Costs](http://i.imgur.com/ehEmfA1.jpg)

Granted, this diagram refers to the "old" ("waterfall") way of writing software, the amount of time spent maintaining code still often exceeds
the time spent initially developing it using a modern "agile" methodology. As such learning to read code is at least as important as learning to write it.

We must *practice* reading code and paying ***close attention to detail***.

## How we conduct code reviews

### 1. Locate the GitHub repository you are planning to review

The first step is locate the repository for the code you are going to be reviewing. If you can't find the code, you don't have much hope of reviewing it... (* this is obvious but you would be surprised how many times people have requested code reviews and failed to provide a link to the repo*...)

### 2. Overview of Files in the repo

Have a quick read through the list of files in the repo.

+ is there a **README.md** or other documentation?
  + Follow the instructions in the README.
+ Does the project have a "manifest" file
(e.g. package.json or component.json or bower.json)
  + Clone the repo and attempt to run the code e.g:
  `npm i && npm test`

if either of these two files are not present, go straight to the issues section of the repo and check if someone else has already raised this as an issue. If no issue exists highlighting the lack of documentation, raise one.

### 3. Quick Check or Detailed Review?

Gauge what level of review is required.  
Are you doing a detailed review prior to delivering a sprint to a client or deploying a major version to many 'users'?
Or is this an small/incremental change small enough for you to understand everything that has changed in 20mins (or less) of reading?

Do you have access to the "user" stories / acceptance tests, to know if the code has solved the problem as it was originally identified?

### 4. Large Project? > Focus on the files that are changing the most

If you are new to the project, it can be overwhelming and you might not know where to start looking in the codebase. If the project organisation is not *obvious* after 5 minutes of inspection, call for help.
If the code author(s) are available, try to pick their brains and request a walk-through (either in person or remote. e.g: google hangout)

### 5. Raising issues

The main branch of a repository should be "*stand alone*".
By this we mean it should be self-explanatory (without further clarification from the original creators).

Raise issues if you spot any gaps in clarity in the code or documentation.

#### Etiquette

As the person reviewing code, always phrase your issues in an open-minded way (*avoid "this is bad code" type issues, they are useless*) use questions and *seek to understand*.

If you (*think* you) know a "better way" of solving a problem, phrase the issue as a question: e.g:  
"*Would you consider using `this` here instead of `that` because of xyz reason...?*"

If you are referring to a section of code, provide a full link to the line(s) including the branch/commit id. e.g: https://github.com/foundersandcoders/beekeeper/blob/e92ef2d3625ea5e5f7cf29e7daa11c86fa3741bd/test/auth.test.js#L20

Tip: if you want to keep links short, use http://git.io/

If you are reviewing a Pull Request add line-comments: https://help.github.com/articles/commenting-on-the-diff-of-a-pull-request/ so that your feedback is contextual.  

#### Guide: Ask yourself (*the code author*) the following *Questions*

+ Does the commit history tell a coherent story?
+ Does this pass the "everyone on the project gets abducted by aliens" test?
+ Does the repository have tests? (*if not, red-flag it*)
+ Do the tests pass? (following the instructions in the repo's readme) e.g: `npm i && npm test` (*for node.js based projects...*)
+ Are all ***dependencies explicitly declared***?
+ Are installation instructions complete?
+ Are instructions for running tests complete? (*try running the tests!*)
+ Is `npm start` script defined in `package.json` (*node.js projects*)
+ Do you understand the *point* of all the tests? (are there are any "tests" without assertions?)
+ If the *code coverage* is incomplete, why is that?
+ Does all the code pass "lint" checker? (see: [jshint](https://github.com/docdis/learn-jshint));
+ Is the file/project structure clear?
+ Are any of the **files** ***too long*** (~200+ lines);  
+ Is the code  "[***DRY***](http://en.wikipedia.org/wiki/Don%27t_repeat_yourself)"
(*i.e: limited repitition*)
+ Could the code be more modular?
+ Are any functions poorly/confusingly named?
+ Could a comment be removed if your function was better named?
+ Do any of your functions do more than one thing?
+ Will factoring out any of your code make yout functions easier to read?
+ If any of the functions look hard to test (*or* ***are untested***!);
+ Are any variable names not being declared at the top of the block in which they are used (why is this important?)
+ Is the code appropriately commented?
+ Is indentation consistent?
+ Is the flow of the program clear? (are there too many branches?)
+ Are any callbacks without error checking?
+ Are any functions too-deeply nested (any signs of "callback hell")?
+ Are there any username/password or secret/api keys or credentials in the code? Flag these!

## Background Reading

+ Is code for computers or humans?
http://stackoverflow.com/questions/522828/is-code-for-computers-or-for-people
+ Writing code for humans:  https://medium.com/@ilyothehorrid/writing-code-for-humans-5b80a89f439c
+ ***Maintainable*** JavaScript:
https://github.com/jasonzhuang/tech_books/blob/master/js/Oreilly.Maintainable.JavaScript.May.2012.pdf
+ JavaScript the ***Good Parts*** Notes:
https://github.com/iteles/Javascript-the-Good-Parts-notes
+ Writing code for humans:
https://medium.com/@ilyothehorrid/writing-code-for-humans-5b80a89f439c
+ Curly's Law: Do One Thing:
http://blog.codinghorror.com/curlys-law-do-one-thing/
+ Write/Read-only Code: http://en.wikipedia.org/wiki/Write-only_language
+ Spaghetti Code:
http://en.wikipedia.org/wiki/Spaghetti_code
+ Code Refactoring:
http://en.wikipedia.org/wiki/Code_refactoring
+ How To Write Unmaintainable Code (*ensuring job security*):
https://thc.org/root/phun/unmaintain.html  
(*this is informative not instructional*...)
