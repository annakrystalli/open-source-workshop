# Cloning and collaborating: contributing changes

[[<<PREVIOUS: Let's get started with Git and GitHub]](git-01-lets-get-started-with-github) -
[[Table of Contents]](../../index) - [[NEXT: Cloning and collaborating: managing contributions>>]](git-04-more-cloning-and-collaborating)

So far, we've learnt how to create repositories, commit files, and push/pull the files to a remote source like GitHub. Here we'll practice collaborating with someone else. There are two approaches to collaborating on GitHub:

## 1. Forking, cloning, and pull requests

If your code is online on GitHub and has an open licence, anyone can [fork](https://help.github.com/articles/fork-a-repo/) (make a separate copy of) your repository and work on it. 



<img src="assets/clone.jpg" width="700px" />

<small>_[Source](https://github.com/jlord/git-it/blob/master/guide/assets/imgs/clone.png) (c) Jessica Lord, [BSD-2](https://opensource.org/licenses/BSD-2-Clause)_</small>

<br>

Let's explore forking and cloning a GitHub repository through a fun exercise.


###  **EvoLottery: Welcome to the evolutionary lottery of skull and beak morphology**

> [**Beak and skull shapes in birds of prey (“raptors”) are strongly coupled and largely controlled by size.**](http://eprints.whiterose.ac.uk/99452/1/Bright%20et%20al.%202016_SelfArchive.pdf) _Bright, J.A., Marugan-Lobon, J., Cobb, S.N. et al. (1 more
author) (2016) The shapes of bird beaks are highly controlled by nondietary factors. PNAS, 113 (19). pp. 5352-5357._

![](assets/gif.gif)

gif provided by **Jen Bright** [**@MorphobeakGeek**](https://twitter.com/MorphobeakGeek)

#### Exercise aims

- In this exercise, each participant will **fork a GitHub repository**, and **contribute a file** required to simulate the *evolutionary trajectory of an imaginary species' body size*.

We'll merge all contributions and [plot them together at the end!](http://rse.shef.ac.uk/collaborative_github_exercise/plot_trait_evolution.html) 


- We'll use **GitHub to collate all species files** and **plot** them all up together at the end! We'll also **discover the skull and beak shapes** associated with each simulated species size.

<br>

---


### **Fork a repository on GitHub** 

<br>

#### **Navigate to the repository**

<https://GitHub.com/RSE-Sheffield/collaborative_GitHub_exercise>

<img src="assets/repo.png" width="700px" />

<br>


##### **Fork the repository**

Make your **own copy of the repository** on GitHub. Forks are linked and traceable

<img src="assets/fork-1.png" width="700px" /> 


<br>

When forking, GitHub makes a **copy of the repository into your account**

<img src="assets/fork-2-gk.png" width="700px" />
 

<br>

### **Clone a repository using GitKraken** 


<br>

#### **Clone your fork**


<br>

Now that you have a fork in your account, let's clone it (ie download a local copy) through GitKraken.

To start clonining, go to: `File > Clone Repo`

<img src="assets/clone-1-gk.png" width="700px" />

<br>

In the **Clone** panel, select **GitHub.com** from the source panel. The right-side panel allows you to define the final details of the clone:

- __Where to clone to:__ Select the folder where the repository will be cloned to. Let's say _D:/GitHub_.

- __Repository to clone:__ Here you'll see a list of all the repositories you have access to and which you can clone. Choose the repository named _collaborative-github-exercise_.

- __Full path:__ Here GitKraken will show the full path where the repository will be cloned to. This will be _D:/GitHub/collaborative-github-exercise_.


<img src="assets/clone-2-gk.png" width="700px" />

<br>


When you're done specifying what and where to clone, click on **Clone the repo!**. If everything worked, you should see the following screen:

<img src="assets/clone-3-gk.png" width="700px" />


<br>

Click on open **Open Now** to view the version control activity associated with the project you just cloned. Git has been tracking the full history of the cloned repo, including all the changes made and who they were made by. 


<img src="assets/clone-4-gk.png" width="700px" />

<br>

The cloned repository contents should look like so:

<img src="assets/clone-5-gk.png" width="700px" />

<br>

---

### **Make a change to the repository**

For this exercise each participant will create a single new file, setting a few parameters to values of their choice, in their fork. We will then collate everyone's files in the original repository through **pull requests**.

The **`params/` folder is where we are going to gather our individual parameter files**. Currently, it just contains a **`.R` template file called `params_tmpl.R`**. Please **DO NOT EDIT this file**. We will **make a copy** of this file to edit. Let's go ahead and create and complete these files:
 
<img src="assets/param-folder.png" width="700px" /> 
 
<br>

#### Make a copy of **`params/params_tmpl.R`**

First think of a species name based on your name, eg _Augustinus vourinous_. This will be the species name associated with the evolutionary trajectory defined by the parameters you're going to supply. This is both for for fun, but also to ensure that the files each participant commits has a unique name.

Now, make a copy of the file and save it in the same folder (`params/`). Use the species name you came up with to name the file.

<img src="assets/copy-param-tmpl.png" width="700px" />

<br>

#### Edit your parameters file with values of your choice 

Open the file you just created in your favourite text editor, edit it with parameters of your choice and save.

The parameters each participants need to supply are:

- **`sig2`:** A numeric value greater than 0 but smaller than 5

- **`species.name`:** a character string e.g. `"anas_krystallinus"`. Try to create a species name out of your name! It must be enclosed in double quotes (ie `"..."`)

- **`color`:**  a character string e.g. `"red"`, `"#FFFFFF"` (Check out the list of available [**colours in R**](http://www.stat.columbia.edu/~tzheng/files/Rcolor.pdf)). It also must be enclosed in double quotes (ie `"..."`)

**NB: remember to save the changes to your file**

<img src="assets/param-complete.png" width="700px" />

<br>

---

### Commit changes locally to git

#### In GitKraken, stage the new file you created

Moving back to GitKraken you should now see that there is one file containing changes and that it is the new parameters file you just created.

To **add (stage) this file to the commit** we are about to make, click on the **Stage File** button next to the name of the file. Please **ONLY STAGE YOUR NEW FILE** (ie if for any reason you've accidentally edited any other file in the repo, please do not stage it).

<img src="assets/commit-pre.png" width="700px" />


<br>

#### Commit the staged file

The file has now moved to staging area. Were now ready to commit it. Before that we need to provide a **descriptive commit message** that explains what the changes contained in this commit are.

Once you've written an appropriate commit message, you can go ahead and click on **Commit changes** button to commit the file.

<img src="assets/commit-param.png" width="700px" />

The changes have now been committed locally to git but you still need to update your remote fork on GitHub. We'll do this by pushing our local changes to GitHub

<br>

---

### Push changes to your fork GitHub

Now that you have made the commit, you now see the details of that commit in the right hand panel. To push the commit to your fork on GitHub, click on the **Push ⇧** button. Your changes have now been updated in your GitHub repo!

<img src="assets/commit-push.png" width="700px" />

<br>

---

### Make a pull request to the upstream repository

Tha changes you made locally have now been committed and pushed to your fork on GitHub. If you go to GitHub, you'll now be able to see the details of the last commit. However, we **want to collect all participants' files in the upstream repository** ie `RSE-Sheffield/collaborative_github_exercise`. So the next step is to **make a pull request** from your fork to the upstream repository. 

<br>

#### Initiate a new pull request

GitHub is already flagging the fact that your **fork is ahead of the `master` branch** in the upstream repository and a **button to make a new pull request** with your changes is visible above that flag.

To initiate a pull request (PR) just **click that `New Pull Request` button**. 

<img src="assets/pr-1.png" width="700px" />

<br>

#### Check that changes can be merged

Once a PR is initiated, GitHub automatically compares your version of the code to that in the upstream repository and checks whether your changes can be merged automatically, ie that they do not create any [merge conflicts](https://help.github.com/articles/about-merge-conflicts/). 

If everything has gone well, GitHub should advise that you are able to merge your changes. To continue, click on the **Create pull request** button.

<img src="assets/pr-2.png" width="700px" />

<br>

#### Create pull request

You are finally ready to send the pull request to the upstream repo. The pull request not only shows the changes you made but also **initiates a comment thread in which you can communicate with the upstream repository owners**.

At this stage, you have the opportunity to give a bit more detail about the changes you have made. Be polite and friendly and be as descriptive as possible! Remember, **there are actual humans at the other end of the PR** that need to understand what changes you have made, why and be convinced that your changes are worth merging in to the code base.

<img src="assets/pr-3.png" width="700px" />

<br>

---

### Response from the upstream repo owners

Once a PR is made, it isn’t automatically accepted. The repository owner doesn’t have to accept it, and they might even ask for changes or refuse it outright if the pull request has errors or doesn’t suit them for some reason. The owner of the upstream repository now has the opportunity to digest your pull request through a variety of tools. 

<br>

#### facility to inspect changes

For starters they have the opportunity to **inspect the changes** you have made to the code by clicking on the PR **files changed tab**. In this case they can clearly see that a whole new file was added. They can also check that the changes won't break the existing code. In this case they might check that the parameters submitted follow the guidelines set out in the exercise, ie that colour is a character vector enclosed in `"..."`. This testing process is what continuous integration systems are designed to automate.

<img src="assets/pr-filechanges.png" width="700px" />

<br>


#### facility to to respond to suggested changes

They also have an opportunity to discuss your changes in the **conversation tab**. Perhaps they are unclear about something or maybe they spotted something that needs changing. 

More often than not, you'll get a big THANK YOU! for your contribution and maybe even a :raised_hand: emoji!

<img src="assets/pr-response.png" width="700px" />

<br>

#### merge your changes

Once they are happy with your changes they can go ahead an merge them by clicking on the **Merge pull request** button.

This creates a new commit in the upstream repository, documenting the merge of your changes into thhe upstream code base.

<img src="assets/pr-merged.png" width="700px" />

<br>

---

### Inspect your changes in the upstream repository 

You can now check the upstream repository to see **your merged changes**. The root of the repository indicates that the last commit was the merge of your pull request into the master branch:

<img src="assets/merged-repo.png" width="700px" />

Navigating to the `params/` folder, you should now see the params file you created with your original commit associated with it!


<img src="assets/merged-params.png" width="700px" />

<br>

---


### Exercise recap:

- **fork the repo**: <https://GitHub.com/RSE-Sheffield/collaborative_GitHub_exer
- **create a new params** `.R` script. Name it using your selected species name.
- **enter parameters** for your species.
- **commit & push** your changes
- **create a pull request** to the upstream repo

We'll merge all contributions and [plot them together at the end!](http://rse.shef.ac.uk/collaborative_github_exercise/plot_trait_evolution.html) 


Last tip: You can actually [make pull requests in GitKraken](https://support.gitkraken.com/working-with-repositories/pull-requests)!

<br>

***

---

### The other way to collaborate - give someone repository access rights!

If you are working in a team with others you trust, you can edit repository settings so everyone who is working on the code can make commits directly to the same repository. Sometimes people will do this for small fixes, typos, etc. but still make pull requests for bigger changes - this allows collaborators to review your code before it's merged into the main codebase, ensuring it has enough documentation and test it for bugs.

To add a collaborator to your repository, in your GitHub repository online, go to the settings tab (top leftish), then click on the "Collaborators and teams" link on the left. 

[[<<PREVIOUS: Let's get started with Git and GitHub]](git-01-lets-get-started-with-github) -
[[Table of Contents]](../../index) - [[NEXT: Cloning and collaborating: managing contributions>>]](git-04-more-cloning-and-collaborating)
