# Let's get started with Git and GitHub through GitKraken

[[<<PREVIOUS: What is version control]](../../02-what-is-version-control) -
[[Table of Contents]](../../index) - [[NEXT: Cloning and collaborating>>]](git-02-cloning-and-collaborating)

<img src="assets/gk01a.png" alt="title picture" width="700px">

We'll be using [GitHub](http://www.github.com) and [GitKraken](https://www.gitkraken.com/). If you don't already have a GitHub account, please register for one now at [github.com](http://www.github.com).

Next, let's get started on some practical exercises.

## Creating your first repository

This process can be done with an existing project that isn't in git yet, or a
new project. We'll start by creating a new repository to get the feel for things.

1. In GitKraken, make sure you're logged in to GitHub.
2. Create a new repository (File > Init Repo)

	<img src="assets/init-1-gk.png" alt="title picture" width="700px">

3. You will be presented with a new GUI with a bunch of options.

	<img src="assets/init-2-gk.png" alt="title picture" width="700px">
	\
	- __Account:__ In which account you want the repository to be created to. This can be your account or an organization that you have access to.
	- __Name:__  The name of the repository let's say _git-lesson_.
	- __Description:__ Optional, but every repository should have a small description!
	- __Access:__ Public or Private.
	- __Clone after init:__ This checkbox tells GitKraken to run the clone procedure. This essentially creates a copy of the repository to the folder you will specify afterwards.
	- __Where to clone to:__ Select the folder where the repository will be hosted if selected to be cloned. Let's say again _D:/GitHub_.
	- __Full path:__ This should now be _D:/GitHub/git-lesson_
	- __License:__ A license is mainly a list of permissions that other people who want to use your code can do. For example you may want others to use your code but only if they accredited you. [choosealicense.com](https://choosealicense.com/) can help you choose the right license. For open source repositories MIT and GNU GPLv3 are usually appropriate licenses.

	<img src="assets/init-4-gk.png" alt="title picture" width="700px">

4. Let's have a look at: 

	1. the repository's history in GitKraken, 
	2. our local version of the repository and 
	3. the repository in GitHub.

	<img src="assets/init-5-gk.png" alt="title picture" width="700px">

Okay! Now we need to do something with the repository. Let's start with a basic use-case and make a single file that lists some to-do items. The repository is just a normal folder on your computer where you can create and edit files like normal.

## Add a file to the repo

1. Open the folder which hosts the repo you have just created. This can be done using GitKraken, just go to File > Open in File Manager. 

	<img src="assets/work-1-gk.png" alt="title picture" width="700px">

2. Now create a file in this directory, you can also drag and drop files or folders. For this example let's say that we create the file *TODO.txt*.

	<img src="assets/work-2-gk.png" alt="title picture" width="700px">

3. Hop over to GitKraken again. You should see the new file you added! 

	<img src="assets/work-3-gk.png" alt="title picture" width="700px">

4. Now it's time to **commit** you work. This is creating a *save point* you can come back to at any time. Aim to do this whenever you've done a small, complete chunk of work. GitKraken provides an easy to use interface for this job:
	\
	- __Unstaged Files:__ Here you have a view of all the local changes of your repository. You can also see the changes done to each file by just clicking on it. You have the option to **stage** all the changes or some of them. Staging is essentially a commit preparation process.
	- __Staged Files:__ All files or folders which are selected to be committed will be moved in this area.
	- __Commit Message:__ Commit creates a save point and every save point should have a title as well as a small description so we know why it was done. Remember some projects last for years and many other projects will spawn in the meantime. So when we revisit an old  repository or we want to go back in time to find a specific change we should be able to do that with minimum effort!
	- __Commit changes to n files:__ Pressing this button will commit our changes *to our local repository*.

	<img src="assets/work-4-gk.png" alt="title picture" width="700px">

5. 	Now that we have commited our changes locally we have to **push** them up to the remote repository. This is done by pressing the **Push** button on the top of GitKraken.

	<img src="assets/work-5-gk.png" alt="title picture" width="700px">	


## Check out the Git history
Now, if you look at the history of the repository you can see two commits. The first was automatically done by GitKraken when you created the repository - and the second should be yours!

<img src="assets/work-6-gk.png" alt="title picture" width="700px">	


## Make some more changes

1. We've gotten some work done, so we'd like to update our to-do list.
  - Update the list with all the tasks we have completed.
  - Add any pending tasks

2. Commit and push the changes in the TODO.txt. *Don't forget to type a summary message* before you commit!

<img src="assets/work-7-gk.png" alt="title picture" width="700px">	

<img src="assets/work-8-gk.png" alt="title picture" width="700px">	


## Pushing and pulling to a remote source

**Push** makes sure that your work is not only in your computer but "online" which means:

  - It is backed up.
  - You can access it from any location.
  - If your repository is open, other people can benefit from your work, they can contribute, reference you or even make recommendations.
  
Now, what if you you make changes directly on the GitHub repository or using another machine ? These changes are not locally synchronized with your primary computer. This is where **pull** comes into play.  

1. Navigate to your repository in GitHUb and check *README.md*. GitHub automatically uses this file to create the long description of this repository which at the moment should be a mere *git-lesson*. To edit this file click on the small pencil icon. This icon is available for any file if you click on it but specifically for README.md it's also available as soon as you enter your repository.

	<img src="assets/work-9-gk.png" alt="title picture" width="700px">	

2. Now let's add some text, *Markdown* text.

	<img src="assets/work-11-gk.png" alt="title picture" width="700px">

3. Let's see how our Markdown code is rendered and check for typos in the text. If we are happy we can commit the changes. Since we are working online on GitHub there is no **push**.

	<img src="assets/work-10-gk.png" alt="title picture" width="700px">

4. Now back to GitKraken we see that our remote repository is ahead of our local. We can also check out local README.md file and we will see that it is not updated. In order to synchronize the remote with the local repositories we have to use **Pull**. This will "download" any updates on the remote repository to our local one.

	<img src="assets/work-12-gk.png" alt="title picture" width="700px">

5. Let's seen what happened after pulling the remote repository.

	<img src="assets/work-13-gk.png" alt="title picture" width="700px">



## Minor note about the differences between Git, GitHub, and GitKraken

Git, GitKraken, and Github are three separate things. Git is the system used for version control, but you don't have to use it with GitHub or GitKraken.


**Git:** version control software. Usually accessed via the command line, or a client program.

**GitHub:** a website that allows you to store your Git repositories online and makes it easy to collaborate with others. They also provide other services like issue (bug) tracking and wikis. Similar services are [GitLab](https://gitlab.com) and [BitBucket](https://bitbucket.org/).

**GitKraken:** A client for working with Git that uploads your work to GitHub. Another is [SourceTree](https://www.sourcetreeapp.com/), and there's a [big list of clients on the git website](https://git-scm.com/download/gui/windows).


[[<<PREVIOUS: What is version control]](../../02-what-is-version-control) -
[[Table of Contents]](../../index) - [[NEXT: Cloning and collaborating>>]](git-02-cloning-and-collaborating)
