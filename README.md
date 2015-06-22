![General Assembly Logo](http://i.imgur.com/ke8USTq.png)

## Objectives
- Use `git init` to create a repository.
- Use `git diff`, `git add`, and `git commit` to create new snapshots in the repository.
- Use `git clone` to copy a repository.
- Use `git reset` to 'turn back the clock' on a repository.
- Use GitHub to fork and clone a repository.
- Use GitHub to submit a pull request.

## Prerequisites
- Complete Chapter 2 of Fundamentals.

## Overview :: Version Control

Have you ever worked on a document - say, a resume - and produced a dozen different versions of it? What a pain. Not only do you need to keep track of what changes you make each time, you need a reasonable system for organizing and managing all of the different versions. Now imagine that you had 50 different versions, with multiple contributors, and that the document you were editing was 20 to 30 thousand lines long. Yeesh.

Software projects are made up of a **ton** of code, and often projects are so large, require so many iterations, and involve so many people that version control isn't a luxury - it's a **necessity**.

## Git
### Browsing Through History

Git is a version control tool designed by Linus Torvalds, the guy who invented Linux; it works by allowing users to create 'snapshots' that represent the state of the project (called a **repository**) at any moment in time.  

To look at that series of snapshots for any given Git repository, we simply need to navigate into the repository using the terminal and run the command `git log`. This will print out a sequential list of the snapshots (often causally referred to as _commits_) that have been made. Neat!

![Git Log](images/git_log.png)

Each commit refers back to the state of the repository at a previous commit, like so:

![Git Commits - Before New Commit](images/commits_before.png)

`master` on the right is what's called a _branch_ - a reference that points to a particular commit. When new commits get made on the `master` branch, they get added to the end, and `master` is updated so that it points to the new commit.

![Git Commits - After New Commit](images/commits_after.png)

> We'll be learning more about branches later in the course, so don't worry too much about them right now.

Of course, while it's interesting to be able to see a list of the snapshots, the system isn't very useful unless it actually allows us to revisit those old snapshots (and, if necessary, revert to them). Note the `HEAD` reference in the diagrams above: `HEAD` refers to the version of our project that we're currently 'reading' from the repository - in other words, the current state of our project if we were to look inside our directory. By moving the `HEAD` reference, we can effectively go back in time and see how our repository looked in a previous snapshot.

The command to do this is `git checkout x`, where x is the alphanumeric name for a particular commit. Say we wanted to check out the state of the repository at commit 07bc287.... ; typing

`git checkout 07bc2871c495f508c03b0c25df2aca8484ab2c08`

would move `HEAD` so that it pointed to the previous commit.

![Detached HEAD](images/detached_head.png)

If we open our project in Sublime, we can see that the clock has been turned back. Awesome! Unfortunately, it's a "look, don't touch" sort of thing - while we're in what's called 'detached HEAD' mode, it's not possible to make new commits. However there are other commands that let us do that... but first, let's look at how snapshots get made in the first place.


### Lab :: Sub-Topic 1

## Sub-Topic 2

### Lab :: Sub-Topic 2

## Sub-Topic 3

### Lab :: Sub-Topic 3

## Further Reading
-
