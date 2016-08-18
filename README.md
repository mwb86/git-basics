[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Git Basics

## Objectives

-   Initialize a git repository in order to track changes.
-   Create a new branch to isolate your changes.
-   Place new or changed files into the staging area to prepare them for a
commit.
-   Remove files from the staging area before a commit.
-   Commit new and changed files to a git repository.

## Prerequisites

-   [WDI Fundamentals, Chapter 2](http://fundamentals.generalassemb.ly/02_chapter/intro.html)

## Why Git

Version control! As developers our code is our livelyhood so it's important
that we safely store our work... frequently.  Not only that we want to track our
changes as we make them.  If we make a feature that ends up breaking the rest of
our app we want to be able to go back to a point when our app was last working.

## Code Along: Making a Local Repository

Let's initalize a local repository.

1.  In your training directory create a subdirectory called `game-of-gits`.

1.  Inside of the `game-of-gits` directory create a file called `sad-tale.md`.

1.  Opening the file with Atom copy in the following lines:

  ```bash
  House Stark of Winterfell is led by the just Eddard "Ned" Stark, Lord of
  Winterfell, Warden of the North, Hand of the King, Protector of the Realm,
  Regent.  He is surely honorable and will lead a long and prosperous life.
  ```

1.  Save the file.

1.  Inside of the `game-of-gits` directory type `git status`. Did anything
happen?

1.  Again, inside the `game-of-gits` directory type `git init`.

1.  Type `git status` again. Did anything happen this time?

## Code Along: Staging and Commiting

Using `git add <"name_of_file">` we are going to add our story to the staging
area.

There are 3 states that your file can reside in `committed`, `modified` and
`staged`.  These states map to the different sections of a Git project.

-   Committed means that the data is safely stored in your local database.
-   Modified means that you have changed the file but have not committed it to
your database yet.
-   Staged means that you have marked a modified file in its current version
to go into your next commit snapshot.

[Git Basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)

![Git Sections](https://git-scm.com/book/en/v2/book/01-introduction/images/areas.png)

When we add a file we are moving it from the working directory to the staging
area.

Now that our file is staged let's commit our file by typing `git commit`, Atom
should open. **Do Not Use `git commit -m <message>`**

When you use -m to create an inline commit you are doing yourself and others a
disservice.  Your commit will be inherently poor due to the short nature of
inline commits, and the lack of a body description to it. This is surely a sign
of a poor developer and one that does not respect his or her teammate's time.

## Lab: Crafting A Commit

Read over the following blog posts and carefully think about what a good commit
message would be. Take some time to come up with your own. Be ready to share
your commit with the rest of the class.

-   [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
-   [What's in a Good Commit?](http://dev.solita.fi/2013/07/04/whats-in-a-good-commit.html)

Now that we've made our first commit, let's see what happens when we type `git
log`... We see our previous commit! This typically shows all of our previous
commits, but since we just have one, that's all we see. Feel free to play around
with options for `git log`, like `--oneline`, `--name-status`, and `--graph`
for example. For all options [click here.](https://git-scm.com/docs/git-log)

## Staging: And He Lived Happily After

Together, let's continue our story.

In our `sad-tail.md`, we'll tell the rest of Ned Stark's story.  Paste this in
below our current description and save:

```sh
Ned Stark went to King's landing where he made lots of friends and lived
happily ever after...  He definitely didn't get axe murdered.
```

Now using what we learned earlier stage this change. To figure out the status
of your files you can type `git status` in the terminal at any time.

**Remember: Staging isn't commiting**

## Unstaging: Maybe We Jumped the Gun

It turns out Ned actually did get axe murdered. So we probably want to unstage
our file.

Unstage the file with `git reset <"filename">`

Delete the last thing we wrote in `sad-tail.md`.

We know that Ned's story doesn't have a happy ending but let's dream big.  We're
going to create a dream-story branch and write what we would have wanted to
happen.

## Removing: Now we need to remove files previously added

1.  Inside of `game-of-gits` create a file called `the-stark-bunch.md`.

1.  Type `This is a story... of a man named Neddy... and three
very badass really awesome girls`.

1.  Save the file.

1.  `git add very-bad-tale.md`.

1.  `git rm --cache very-bad-tale.md`.

1.  `git add very-bad-tale.md`.

1.  `git rm -f very-bad-tale.md`.

What's the difference? What is actually happening with the `rm` command?

## Branching: Multiple Stories, One Main Plot

Similar to having one main story and various sub-plots--a branch lets us
effectively duplicate and section off the code we have writte thus far, make
alterations to it, and if we would like at some point we can join it back to the
main branch (typically called `master`).

Create a branch called `dream-story` by typing `git branch dream-story`.
_You can see all your current branches at any time by tying `git branch`._

Now that we've created our branch--in order to use it we have to switch to it.
We can do this with the command `git checkout <"branch_name">`.

## Lab: Branching Your Dreams

1.Switch to your `dream-story` branch and write a brief description of what
you would have wanted to happen to Ned.

2.Save the file, Stage and commit your changes.

3.Switch back to your `master` branch. (Notice anything?) Add what really
happened to Ned.

4.Stage and commit your changes.

(Be ready to talk about any issues you many have encountered or strange things
you may have noticed).

## Git Workflow Checklist

-   [ ] `git status` to confirm clean working directory
-   [ ] confirm branch is correct
-   [ ] make changes to `file`
-   [ ] `git add 'file'`
-   [ ] `git status` (to confirm modified files have been staged)
-   [ ] `git commit`
-   [ ] `git push origin <branchname>`

## Git Best Practices

-   NEVER use `git add .`
-   ALWAYS add files explicitly. If you have multiple files, use full paths to
    refer to each. Example: `git add foo/bar.md baz/qux.js`
-   NEVER use `git commit -m "an example commit message"`
-   ALWAYS use `git status` before any other command
-   NO commit is too small
-   NO commit message is too long
-   NEVER nest repositories

## References

-   [Git Commands Cheatsheet](command-reference.md)
-   [Learn Version Control with Git](http://www.git-tower.com/learn/git/ebook)
-   [Visualizing Git Commands](http://www.wei-wang.com/ExplainGitWithD3/)
-   [Learn Git Branching](http://pcottle.github.io/learnGitBranching/)

## [License](LICENSE)

Source code distributed under the MIT license. Text and other assets copyright
General Assembly, Inc., all rights reserved.
