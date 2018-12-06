# More cloning and collaborating: managing contributions

[[<<PREVIOUS: Cloning and collaborating: contributing changes>>]](git-03-cloning-and-collaborating) -
[[Table of Contents]](../../index) - [[NEXT: Websites with GitHub pages>>]](git-02-websites-with-github-pages)

In the previous exercise you practiced forking and cloning someone else's repository and contributing changes. In this exercise you'll get the opportunity to have others submit pull requests to your repository and merge them in!

1. For this exercise, team up with someone near you. Share the URL of your repository with your team-mate.
2. Go to your team-mate's repository on GitHub. Click on the Fork button on the top right of the page.
3. Once the repository has successfully forked, you'll need to [clone](https://help.github.com/articles/cloning-a-repository/) it onto your machine if you want to edit it. In GitHub desktop, go to `File > Clone a repository`. You should be able to find the repository you forked earlier. Select it and press "Clone".
4. You should be able to work on the repository as normal now. Edit the file and make a commit - maybe you've helpfully taken something off your team-mate's to-do list, or maybe you've fixed a typo in their documentation or helped them fix a bug.  
5. Push the changes to GitHub, then go and look at your team-mate's repository on GitHub. If you see a yellow notification offering to help you make a pull request, click it and move to step 6! If not:
  - Click on the "Pull requests" tab on the top, and then click the "new pull request" green button on the top right.
  - You may need to click compare across forks (blue link, top rightish).
  - The **base fork** should be your team-mate's repository
  - The **head fork** should be _your_ fork of the repository, where you've made the extra commit.
  - Click create new pull request.
6. Okay, now you should enter a description for your pull request - this might be the same as the commit message you made or it might be more detailed. This description is for your team-mate to review, so they know why you made the request, so don't skip it!
7. Once you're happy with your pull request description, click "Create Pull Request". That's it - you've made your first PR (Pull request) to someone else's code base!

#### Review your team-mate's PR

Once a PR is made, it isn't automatically accepted. The repository owner doesn't have to accept it, and they might even ask for changes or refuse it outright if the pull request has errors or doesn't suit them for some reason.

1. Once your team-mate has made a pull request online, you should see the number (1) showing beside the "pull requests" tab in your repository. Visit the pull request and take a look through the various tabs
  - In the **files changed** tab you can see _exactly_ what changed in each file
  - The **commits** tab shows all of the commits that go into this specific pull request that aren't present in the base branch.
  - If you're happy with the changes, hop back over to the **conversation** tab and click the big green "Merge pull request" button.
  - If you think there are changes or improvements to be made - leave a polite comment asking for clarification or changes!


[[<<PREVIOUS: Cloning and collaborating: contributing changes>>]](git-03-cloning-and-collaborating) -
[[Table of Contents]](../../index) - [[NEXT: Websites with GitHub pages>>]](git-02-websites-with-github-pages)

