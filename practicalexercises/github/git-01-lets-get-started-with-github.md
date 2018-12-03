# Let's get started with Git and GitHub

[[<<PREVIOUS: What is version control]](../../02-what-is-version-control) -
[[Table of Contents]](../../index) - [[NEXT: Cloning and collaborating>>]](git-02-cloning-and-collaborating)

![](.\assets\gk01.jpg)

We'll be using [GitHub](http://www.github.com) and [GitKraken](https://www.gitkraken.com/). If you don't already have a GitHub account, please
register for one now at [github.com](http://www.github.com).

Next, let's get started on some practical exercises.

## Creating your first repository

This process can be done with an existing project that isn't in git yet, or a
new project. We'll start by creating a new repository to get the feel for things.

1. In GitHub Desktop, make sure you're logged in. (On a Mac this is top left `GitHub Desktop > Preferences`)
2. Create a new repository (File > New Repository)
    - Select any name you like. "git-lesson" would be fine.
    - Tick "initialise this repository with a README"
    - Change the file path if you wish. _take note of this path, you'll need it later_
    - Select the MIT Licence
    - Click "Create repository"


Okay! Now we need to do something with the repository. Let's start with a basic use-case and make a single file that lists some to-do items. The repository is just a normal folder on your computer where you can create and edit files like normal.

## Add a file to the repo.

1. In GitHub desktop, click on `Repository` in the top menu and open the folder where your repository resides. (On a Mac, this is `Open in Finder`). You should already see a LICENCE file that GitHub desktop automatically generated for you.
2. Create a new file in this directory! I've called mine todos.txt, but you could name it anything you like and it can be any type of file. Make sure to save it when you're done.
3. Hop over to GitHub desktop again. You should see the new file you added!
4. Now it's time to "commit" you work. This is creating a "save point" you can come back to at any time. Aim to do this whenever you've done a small, complete chunk of work. On the bottom left of your GitHub Desktop window you should have a box that says "Summary". Type a short sentence describing what you've done into this box. I put "Added To-dos for Monday."
5. Press the big blue "Commit to master" button.

## Check out the Git history
Now, if you look at the history tab, (top left in GitHub Desktop) you can see two commits. The first was automatically done by GitHub Desktop when you created the repo - and the second should be yours!

## Make some more changes

1. We've gotten some work done, so we'd like to update our to-do list.
  - Delete one item from your list.
  - add another two items to the list.
2. If you take a look at the file now, you should see the lines you removed highlighted in red, and all new lines are highlighted in green. This is really handy when you have been making a lot of changes or writing notes. No more "FIX THIS" accidentally being saved in a commit! The representation of changes is also known as the 'diff' (short for difference).
3. Once you're ready, type another summary message and save your commit.

## Pushing and pulling to a remote source.

Right now your work is only on your computer - it's neither open nor backed up yet. Let's publish it on GitHub.

1. In GitHub desktop, you should see a "Publish Repository" in a bar along the top. Click it!
2. Make sure you're happy with the repository name
3. Untick the "Keep this repository private"
4. Click "Publish repository".
5. Go to [github.com](http://www.github.com) and navigate to your new repository. You should be able to see all the files and commits you made previously.
6. On your computer, add another item to your to-do list, then save the file and commit it on GitHub Desktop. If you look at your repository on github.com, has it updated? (Hint: There's a button in GitHub Desktop you'll need to press in order to push it.)
7. You can also edit files on GitHub directly (without using GitHub Desktop). As we've already learned, files don't automatically synchronise with your GitHub desktop client, so you'll need to fetch your changes in GitHub Desktop by clicking the "Fetch" button (this will tell you how many updates there have been, if any), and then click it a second time to pull the changes down onto your computer.

### Minor note about the differences between Git, GitHub, and GitHub Desktop

Git, Github Desktop, and Github are three separate things. Git is the system used for version control, but you don't have to use it with GitHub or GitHub desktop.


**Git:** version control software. Usually accessed via the command line, or a client program.

**GitHub:** a website that allows you to store your Git repositories online and makes it easy to collaborate with others. They also provide other services like issue (bug) tracking and wikis. Similar services are [GitLab](https://gitlab.com) and [BitBucket](https://bitbucket.org/).

**GitHub Desktop:** A client for Git that uploads your work to GitHub. Another is  [SourceTree](https://www.sourcetreeapp.com/), and there's a [big list of clients on the git website](https://git-scm.com/download/gui/windows).

[[<<PREVIOUS: What is version control]](../../02-what-is-version-control) -
[[Table of Contents]](../../index) - [[NEXT: Cloning and collaborating>>]](git-02-cloning-and-collaborating)
