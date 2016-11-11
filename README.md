# Participating in Open Source for Designers

Special thanks to Brian Ford who crafted the original version of this document that was specifically geared to developers.  This version utilizes his framework as a tool to help designers get involved in open source development.

So, let's get started.
You’ll need a place to store and publish your code.  Github is the place. Github helps you track your design process across teams and saves snapshots of your entire codebase, allowing you to easily share work with designers and developers.  There are lots of design tools that try to do this work as well, but being able to utilize the same tools as your developers makes a huge difference in productivity. 
* [Create a github account](https://github.com/join
https://help.github.com/articles/signing-up-for-a-new-github-account/)

Next you’ll need a way to keep track of the changes you make to your code as it is developed:

* [Download and install git](http://git-scm.com/download)

What is git?  Git is open source version control software that helps you track changes to your code as it is developed.  It is the de facto standard for developers to help them keep track of changes in their code.

Next you’ll need to install Node.  Node simply executes your code so that you can view it in your browser
*[Download Node](https://nodejs.org/en/download/)

As part of the installation you just did for Node, a program called NPM was installed.  NPM checks for packages of code on your computer and looks for dependencies on other packages to help you know which versions of code you are working with and help you find what is missing.  

While you can download the Github application for moving files from your computer to Github, it's also really useful to know and understand command line.  
*[Learn how to use command line](https://www.davidbaumgold.com/tutorials/command-line/)
*[Step by step guide for command line](https://try.github.io/levels/1/challenges/1)

##Don't fear mistakes

At first, it's intimidating to publicize your work on GitHub.
Few guides address "how" you should use it in terms of etiquette, best practices, and expectations.
As you read this guide, please keep in mind that it's okay (and even expected!) to make mistakes.
You don't have to memorize every minute detail.
Do the best you can and learn as you go.


## Asking a Question

Before you ask, do some searching and reading.
Check the docs, Google, GitHub, and StackOverflow.
If your question is something that has been answered many times before, the project maintainers might be tired of repeating themselves.

If the project is small, it's usually fine to ask questions on GitHub by filing an issue.
If the project is large, they might have a mailing list or IRC channel that would be a better place to ask.
StackOverflow is also a great resource.
Whenever possible, ask your question on a public forum.
This allows anyone to answer and makes the answer available for the next person with the same question.
If all else fails, you might tweet at or email the maintainer(s).



## Submitting a Bug Report (or "Issue")

In GitHub, "Bug Reports" are called "Issues."

### Has This Been Asked Before?

Before you submit a bug report, you should search existing issues.
Be sure to check both currently open issues, as well as issues that are already closed.
If you find an issue that seems to be similar to yours, read through it.

If this issue is the same as yours, you can comment with additional information to help the maintainer debug it.
Adding a comment will subscribe you to email notifications, which can be helpful in getting important updates regarding the issue.
If you don't have anything to add but still want to receive email updates, you can click the "watch" button at the bottom of the comments.

### Nope, Hasn't Been Asked Before

If you can't find anything in the existing issues, don't be shy about filing a new one.

You should be sure to include the version the project, as well as versions of related software.
For example, be sure to include the version numbers output by the commands `node --version` and `npm list`.
If you notice that your installed version is not the latest, use `npm update` and confirm that the issue is still there.

Project maintainers really appreciate thorough explanations.
It usually helps them address the problem more quickly, so everyone wins!



## Improving the Code

The best way is to "Fork" the repo on GitHub.
This will create a copy of the repo on your GitHub account.

Before you set out to improve the code, you should have a focused idea in mind of what you want to do.

Each commit should do one thing, and each PR should be one specific improvement.

### Forking

TODO: this

`git clone`



### Editing and Testing


Ok, you're ready to start editing the code, right?
Not quite!
Before you start editing, you should create a [branch].
A branch is like an alternate timeline.
You can read more about `git` branches [here].

If you're trying to fix a bug, you might want to name the branch `fix-short-description`.
If you're adding a feature, `feat-short-description` is a good name.

`git checkout -b something`

As you're changing the code, you might want to try it within some app or larger project.

`npm link`,
`bower link`,
or symlinks


As far as code style, just try to imitate the style of existing code.
Don't sweat over this too much.
If the maintainer doesn't like how your code looks, they'll suggest changes.  

Most projects have a set of tests to make sure that the existing functionality of the code stays the same as you make changes.
This helps keep the software stable.

For example, in `npm`.

### Committing and Pushing

`git commit -m "your commit message"`

### Using Your Change

Though it may not be obvious, you can begin using your code in your own projects immediately.



### Getting your Change into the Project

You made your change, tested it, committed it with `git commit`, and want to send it back to the project and have it included in a future version.

To do this on GitHub, you need to submit a "pull request" (PR).

#### Submitting a Pull Request

The golden rule of submitting PRs is to do things the way the project maintainers would want it done.
You can't read the minds of the project maintainers, but you can look what they did in the past.
Considering these things upfront can really help streamlining the process of getting your change accepted.

Simply put: try to imitate the style of the existing code.
Pay attention to the indentation and brace style in the code.
Does the style use or avoid early `return`s?

Code isn't the only thing to take note of.
You should also pay attention to the tense and format of the commit messages.
Some projects prefer commits to be in present tense:

`fixes the bug`

And others prefer past tense:

`fixed the bug`

A good way to check is to use `git log` and read through past commits.

A couple things to keep in mind:

* Don't change the version number of the software (in `package.json` or `bower.json`).
  The project maintainer(s) will take care of this when they decide to release a new version.


If the project is maintained by a corporation, they might have a [Contributor License Agreement (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) in place to avoid legal issues.


Project maintainers may be busy, so give them some time.
Developers involved in open source often contribute to many projects.
It's not uncommon for a developer to receive dozens of issues notifications a day, so be patient.

If they don't reply in a couple weeks, you might add a comment to "bump" the issue.
Something like "ping @ProjectMaintainer" is usually sufficient.
If you still don't hear from them, an email might be a good way to get in contact.


Assuming the maintainer responds, there are three possible outcomes for your PR:

1. It gets merged. Yay!
2. The maintainer asks you to fix something in the PR before they accept it.
  We'll discuss this below.
3. The PR gets closed, and your change is not added.
  Typically the maintainer will give some justification why.
  If you're adding a feature, maybe there's already some way to get the code to do what you want that you didn't notice.
  If it's a bug, perhaps they want to solve the problem differently.
  Regardless, don't let this discourage you.


#### Fixing Issues in the PR

When asked to make a change to a PR, newcomers oft mistakenly close the existing PR and create a new one.
There's no need to do this!
It's easy to update the existing one.

First, make your changes to the relevant file(s).
As you've done before, stage the file with `git add`:

`git add some-file`

Then you can amend your previous commit like this:

`git commit --amend`

This command takes your staged changes and puts it into your previous commit.

To update the commit in your PR, you'll need to force push:

`git push --force`

The `--force` tells `git` that you want to overwrite the previous commit in your GitHub-hosted repository.

Another common mistake is to create multiple commits instead of amending the changes into one commit.

So you create another commit...

http://git-scm.com/book/en/Git-Tools-Rewriting-History


#### My PR was Closed but I Still Want to use my Changes!

**Good news:** even if your change isn't accepted into the contributor's repository, you can still use it.

npm allows you to install from a GitHub repo

```shell
$ npm install user/repo
```

Better yet, you can use your changes while staying up-to-date on the original repo's code.
This is often referred to as "maintaining a fork" of a project.

How does this work?
First, we'll want to add another remote.
Our fork on GitHub has the remote name `origin`.

TODO: note about git remotes
TODO: maintaining a fork (merging "upstream" changes)
TODO: typically there's no reason to publish your fork, you can reference the SHA on github and DL a zip.



## Starting a Project

Before you start a project, please do thorough research that something like what you want to make
doesn't already exist.


### Searching for Existing Projects

```shell
$ npm search
```

Sometimes you find a project that's old and no longer maintained, but otherwise solves your problems.
See the [using a fork](TODO) section above for more info.

<aside>
**Bonus:** Make a list as you go with notes.
If you find a module you like, you can use your notes to improve the "See Also" section of the
modules you found in your research by sending them PRs.
If you don't find a module you like and end up creating your own, you can turn these notes into a
"See Also" section for your module!
</aside>


### Starting a Project

Starting a new open source project should be your last resort.
Why?

**Best Practice:** Don't publish something to `npm` until it has some reasonable minimal functionality.

Remember: you can always use `npm link` or `npm install user/repo`

### Naming the project

If your module is a plugin, it's usually best to prefix it based on what it's a plugin for.
Some projects have guidelines or conventions on how to do this.
For instance, AngularJS components are usually named `angular-something`, Gulp plugins are
`gulp-something`, and Karma plugins are `karma-something`.

### Writing a Readme

A good readme should have the following parts.

# Project Title

One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

A step by step series of examples that tell you have to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc


## Etiquette

People usually leave communities that seem disrespectful.
In order to make sure everyone feels welcome, it's important to treat everyone with kindness and respect.

Most of the time, this isn't a problem.
Occasionally, developers become frustrated, emotions run high, and feelings get hurt.

Below I've outlined a few common patterns I've seen, as well as steps to mitigate them.

### Assume Everyone is Doing Their Best

> "this problem should be obvious to solve! why hasn't it been fixed?"

Maybe the maintainer has other important things in their life that they need to address.
Prioritizing those things over something on GitHub doesn't make someone lazy.
The health, happiness, and wellbeing of the real person on the other end of the internet is much more important than any bug.

One of the strengths of open source is that you can always fork and fix problems yourself.


> "you obviously don't understand what I'm talking about!"

This type of comment especially drives away beginners.
It should be okay for people to make mistakes.

This is also problematic because it puts the blame on others.
Maybe you could explain the issue better.


It's perfectly normal to get frustrated.
Regardless, it's important to consider the perspectives of others.
Community is more valuable than code, and being nice is more important than being right.  
Help others where you can, always.


## Conclusion

I hope this guide will help you as you learn your way around a codebase, become more productive with your developers and learn to scale your designs through open source.  Special thanks again to Brian Ford for his initial framework.
If you have any suggestions, please create a [pull request] - Would love to hear your feedback!


## License
MIT

