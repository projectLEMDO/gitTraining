# Training Tasks and Tutorials

This page helps you get started with git and GitHub for LEMDO. We encourage everyone to begin by using the command line wherever possible, even if you later transition to using a richer environment such as GitHub Desktop.

## TASK 1

In this task, you will learn to check out the repository, create a branch, make changes in that branch, push the new branch to GitHub, and then issue a pull request for your changes.

### TASK 1.1: Check out the repository

In a suitable folder on your local computer, use this command:

<code>git clone git@github.com:projectLEMDO/gitTraining.git</code>

You should see git clone the repository from GitHub to your local drive. Now move into the resulting folder:

<code>cd gitTraining</code>

Check the status of the repository on your local machine:

<code>git status -uno</code>

### TASK 1.2: Create a new branch

From the status command above, you learned that you are in the default branch of the repository, which is the **dev** branch. There is also a **main** branch, which we will ignore for the moment. Now you can create your own new branch. Think of a useful name for it which will not clash with anyone else's branch, perhaps using your git id. In all the commands below, substitute the name of your branch for **martindholmes-training**.

<code>git checkout -b martindholmes-training</code>

This creates a new branch called **martindholmes-training**. At the moment, the new branch exists only on your local computer, but we want the branch to be available to other users, so we're going to set up and "upstream" branch on the server to track this branch:

<code>git push -u origin martindholmes-training</code>
Now your branch is being tracked on the server. If you go to the repository on the GitHub website, you can confirm this.

### TASK 1.3: Make changes in this branch

You'll see that there is a folder in the repository called **people**. Create a new text file in that folder using your GitHub id (fredbloggs.txt), and write a brief introduction to yourself in that file. Now add the file:

<code>git add people/fredbloggs.txt</code>

Now we're going to commit that change and push it to the GitHub server:

<code>git commit people/fredbloggs.txt -m "Added my self-introduction as part of TASK 1."</code>

Note that committing does not send the file to the server; it just sets it up as being ready to send. To send changes, you have to push:

<code>git push</code>

### TASK 1.4: Issue a pull request

Now go to the GitHub site for the repository, click on [Branches](https://github.com/projectLEMDO/gitTraining/branches), and find your branch. You'll see that there is a link for "Issue a pull request". Click on that link, and complete the form to create a pull request. Assign it to a project administrator such as martindholmes or JanelleJenstad.

That's it. You've completed the first task. Now you wait for the project administrator to merge your changes into the dev branch. Meanwhile, you can switch back to the main dev branch on your local machine:

<code>git checkout dev</code>

You will see that the new file you created has now disappeared, because it doesn't exist (yet) in the dev branch. But it's still safe; if you checkout your own branch (<code>git checkout {yourbranchname}</code> you'll see it back again.
