# Branching, Checkout and Merging

When working on an existing project, especially one that involves more than one person, making changes to it requires working off of a copy of the project to ensure you always have a **clean** and **working** version of the project for you and your team to use. This workflow of incorporating new changes can be condensed down into 3 steps:

1. A copy of the master version is made.
2. The required changes are made in the copy.
3. The changes are then brought back into the master version. This step is optional.

The traditional method of implementing the above steps involves creating a copy of the project folder and files and giving it a name relevant to the change being done. This method has it's disadvantages some of which are outlined below:

- Bringing changes back into the master version is difficult especially if the changes are numerous and span multiple files.
- Incorporating changes from other versions, for example a bug/typo fix, once again is cumbersome.
- If step 3 above is not done, it results in your computer being filled with numerous copies of your project.

All of the above problems are easily addressed by using git **branches**.

Let's revisit the 3 steps outlined above and use git terminology to describe how we would accomplish each one.

1. Create a new **branch** from the master branch. **Checkout** this new branch.
2. Create **commits** on this new branch that have all your changes.
3. **Merge** the **commits** or changes from your new branch into the master branch.

We introduced 3 new terms in the steps above, branch, checkout and merge. Let's describe these terms more.

- Branch: This is the git term for a copy of a version. At any point in time in a git project, you are working on a certain branch. For eg., in the basic concepts section you were working on the master branch. Just like a regular copy of something in your computer, every git branch has a name attached to it that you set.
- Checkout: The git term for switching to a different branch. The analogy would be opening the copy that you have made of your project folder.
- Merge: The term used when incorporating the changes of one branch into another. For example, if you want the changes in branch-1 in branch-2, we describe that process as merging branch-1 into branch-2.

Now that we have the theory out of the way, let's get our keyboard/mouse dirty by applying it.

Before we start, take a look at the panel to the extreme left of git kraken.

![](/images/branches-list.png)

The box marked in red in the image above, can be termed the "Branches Panel" and tells me 3 things about the git project:

1. It has 2 branches in it's local repo, **advanced** and **master**.
2. The user is currently on the **advanced** branch as is evident by the green check mark and highlighting
3. There is only one branch in the remote repo. As team members sync their branches to the remote repo, they will appear here.

## Creating a branch

Let's create a branch using git kraken where you will be adding your favorite quote next to your name.

Start by creating a new branch from the master branch.

![](/images/new-branch.gif)

Make sure the name of your branch is relevant to the work you will be doing on that branch. For eg., in the video above I named it "quote_changes".

When you create a new branch in git kraken it automatically puts you in that new branch as should be evident by the change in the green check mark's position. If at any point in your work you need to switch to another branch you can do so by clicking on the 3 dots next to the branch you want to switch to and clicking on the option, "Checkout <insert_branch_name>".

> Make sure to commit or **stash** (you will learn about this feature later) before switching branches.

## Making changes to your branch

Add a commit to the project that modifies the gitters.md file by adding your favorite quote next to your name. Look at line 3 for an example.

## Merging your changes

Bring your changes back into the master branch by following the video below.

![](/images/merging-branch.gif)

And if all goes well you should now have a new commit in git kraken that looks something like,

> merge branch \<insert-your-branch-name-here\> into master

Congratulations! You have successfully created a branch, made some change and merged them into master. Push your changes to github so other people can be enlightened with your quote.
