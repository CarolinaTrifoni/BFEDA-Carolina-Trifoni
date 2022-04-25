# **Git**


A DevOps tool used for source code management. Git is used to track changes in the source code, enabling multiple developers to work together on non-linear development. Linus Torvalds created Git in 2005 for the development of the Linux kernel. 

* Every developer has an entire copy of the code on their local systems
* Any changes made to the source code can be tracked by others
* There is regular communication between the developers

## **Git workflow**

* **Working directory** - Modify files in your working directory
* **Staging area (Index)** - Stage the files and add snapshots of them to your staging area
* **Git directory (Repository)** - Perform a commit that stores the snapshots permanently to your Git directory. Checkout any existing version, make changes, stage them and commit.

## **Branching**

Branch in Git is used to keep your changes until they are ready. You can do your work on a branch while the main branch (master) remains stable. After you are done with your work, you can merge it with the main office.

![](https://i.imgur.com/yc3AyUs.png)


The above diagram shows there is a master branch. There are two separate branches called “small feature” and “large feature.” Once you are finished working with the two separate branches, you can merge them and create a master branch.
Branching means you diverge from the main line of development and continue to do work without messing with that main line.

Git encourages workflows that branch and merge often, even multiple times in a day.

<br>

---
<br>


# **Git Commands**

## **git commit**
This one is probably the most used Git command. After changes are done locally, you can save them by “committing” them. A commit is like local a snapshot of the current state of the branch, to which you can always come back. To create a new commit, type this command in Git Bash:

    git commit -m "<commit message>"

In version control systems, a commit is an operation which sends the latest changes of the source code to the repository, making these changes part of the head revision of the repository.

The "commit" command is used to save your changes to the local repository.

Note that you have to explicitly tell Git which changes you want to include in a commit before running the "git commit" command. This means that a file won't be automatically included in the next commit just because it was changed. Instead, you need to use the "git add" command to mark the desired changes for inclusion.

Also note that in Git (not like in Subversion), a commit is not automatically transferred to the remote server. Using the "git commit" command only saves a new commit object in the local Git repository. Exchanging commits has to be performed manually and explicitly (with the "git fetch", "git pull", and "git push" commands).

## **Important Options**
    
**-m <message>**
Sets the commit's message. Make sure to provide a concise description that helps your teammates (and yourself) understand what happened.

**-a**
Includes all currently changed files in this commit. Keep in mind, however, that untracked (new) files are not included.

**--amend**
Rewrites the very last commit with any currently staged changes and/or a new commit message.


---

## **git clone**

This command is used for downloading the latest version of a remote project and copying it to the selected location on the local machine. It looks like this:

    git clone <repository url>

To clone a specific branch, you can use

    git clone <repository url> -b <branch name>
    


---

## **git fetch**

This will get all the updates from the remote repository, including new branches.


---

## **git checkout**

You can use the checkout command to switch the branch that you are currently working on:

    git checkout <branch name>

If you want to create a new branch and switch to it, you can do it by using this command:

    git checkout -b <branch name>



---

## **git init**

This is the command you need to use if you want to start a new empty repository or to reinitialize an existing one in the project root. It will create a .git directory with its subdirectories. It should look like this:

    git init <repository name>
    
 

---
   
## **git push**
    
Git push will push the locally committed changes to the remote branch. If the branch is already remotely tracked, simply use it like this (with no parameters):
    
    git push
    
If the branch is not yet tracked, and only resides on the local machine, you need to run the command like this:
    
    git push --set-upstream <remote branch> <branch name>



---
    
## **git diff**

You can use this command to see the unstaged changes on the current branch.
If you want to see the staged changes, run the diff command like this:

    git diff --staged

Or you can compare two branches:

    gif diff <branch1> <branch2>
    


---
    
## **git pull**

Using git pull will fetch all the changes from the remote repository and merge any remote changes in the current local branch.


---

## **git add**
    
This is the command you need to use to stage changed files. You can stage individual files:

    git add <file path>

Or all files:

    git add


---
    
## **git branch**
    
Using git branch will list all the branches of the repository. Or you can use it to create a new branch, without checking it out:
    
    git branch <new branch>
    
To delete a branch, run it like this:
    
    git branch -d <branch name>


---
    
## **Tagging**
    
Git tags are used as reference points in your development workflow. For instance, software release versions can be tagged. (Ex: v1.3.2) It essentially allows you to give a commit a special name (tag).
    
There are two types of tags:
    
**Annotated**
    
    git tag -a v1.2 -m "my version 1.4"
    
And **Lightweight**
    
    git tag v1.2
    
They **differ in the way that they are stored**. These create tags on your current commit. The tags names may be used instead of commit IDs while checking out and pushing commits to a remote repo.
    
In order to create a new tag, you have to use the “git tag” command and specify the tag name that you want to create.
    
    git tag <tag_name>
    


---
    
## **git stash**
    
Temporarily stores (or stashes) the changes you have made to the code you are working on so that you can work on something else and then go back and reapply the changes later.

However, by default, Git will not save changes made to untracked or ignored files to a stash.

Git stash takes uncommitted changes (both staged and unstaged), saves them separately for later use, and then undoes them in the code you are working on:

    $ git stash
    Saved working directory and index state WIP on main: 5002d47 our new homepage
    HEAD is now at 5002d47 our new homepage

You can reapply the changes from a stash by using the command git stash pop:

    $ git stash pop
    On branch main
    Changes to be committed:

        new file:   style.css

    Changes not staged for commit:

        modified:   index.html

    Dropped refs/stash@{0} (32b3aa1d185dfe6d57b3c3cc3b32cbf3e380cc6a)


---

## **git merge**

It will merge any changes that have been made to the codebase into a separate branch of your current branch as a new commit.

    git merge NAME-OF-THE-BRANCH

For example, if you are currently working on a branch called dev and you want to merge the new changes that have been made into a branch called new-features, you would run the following command:

    git merge new-features


---

## **git rebase**

Rebasing a branch in Git is a way to move the entirety of a branch to another point in the tree. The simplest example is to move a branch further up the tree. 

To rebase, make sure you have all the commits you want in the rebase on your master branch. Check the branch you want to rebase and type **git rebase master** (where master is the branch you want to rebase).

<br>


---
<br>
    
    
# **How to Squash Commits in Git**
To "squash" in Git means to combine multiple commits into one. You can do this at any point in time (by using Git's "Interactive Rebase" feature), though it is most often done when merging branches.

Note that there is no such thing as a stand-alone git squash command. Instead, squashing is rather an option when performing other Git commands like interactive rebase or merge.
    
<br>


---
<br>

# **Git hooks**

Git hooks are scripts that run automatically every time a particular event occurs in a Git repository. They let you customize Git’s internal behavior and trigger customizable actions at key points in the development life cycle.

Hooks reside in the .git/hooks directory of every Git repository. Git automatically populates this directory with example scripts when you initialize a repository.

Hooks are local to any given Git repository, and they are not copied over to the new repository when you run git clone. And, since hooks are local, they can be altered by anybody with access to the repository.

**Local hooks** affect only the repository in which they reside. Most useful local hooks are:

* pre-commit
* prepare-commit-msg
* commit-msg
* post-commit
* post-checkout
* pre-rebase

The first 4 hooks let you plug into the entire commit life cycle, and the final 2 let you perform some extra actions or safety checks for the git checkout and git rebase commands, respectively.

All of the pre- hooks let you alter the action that’s about to take place, while the post- hooks are used only for notifications.
    
<br>

---
<br>
    
# **What is the best Git branch strategy?**

Git and other version control systems give software developers the power to track, manage, and organize their code.

Of course, every developer and development team is different, with unique needs. Here is where a Git branching strategy comes in.

## **Git Flow Branch Strategy**

The main idea behind the Git flow branching strategy is to isolate your work into different types of branches. There are five different branch types in total:

* Main
* Develop
* Feature
* Release
* Hotfix

The two primary branches in Git flow are main and develop. There are three types of supporting branches with different intended purposes: feature, release, and hotfix.

**Git Flow: Pros & Cons**
    
The Git flow branching strategy comes with many benefits, but does introduce a few challenges.

**The Benefits of Git Flow:**

* The various types of branches make it easy and intuitive to organize your work.
* The systematic development process allows for efficient testing.
* The use of release branches allows you to easily and continuously support multiple versions of production code.

**The Challenges of Git Flow:**

* Depending on the complexity of the product, the Git flow model could overcomplicate and slow the development process and release cycle.
* Because of the long development cycle, Git flow is historically not able to support Continuous Delivery or Continuous Integration.
    
## **GitHub Flow Branch Strategy**

The GitHub flow branching strategy is a relatively simple workflow that allows smaller teams, or web applications/products that don’t require supporting multiple versions, to expedite their work.

In GitHub flow, the main branch contains your production-ready code.

The other branches, feature branches, should contain work on new features and bug fixes and will be merged back into the main branch when the work is finished and properly reviewed.

**GitHub Flow Considerations**

While working with the GitHub flow branching strategy, there are six principles you should adhere to to ensure you maintain good code.

* Any code in the main branch should be deployable.
* Create new descriptively-named branches off the main branch for new work, such as feature/add-new-payment-types.
* Commit new work to your local branches and regularly push work to the remote.
* To request feedback or help, or when you think your work is ready to merge into the main branch, open a pull request.
* After your work or feature has been reviewed and approved, it can be merged into the main branch.
* Once your work has been merged into the main branch, it should be deployed immediately.

**GitHub Flow: Pros & Cons**

As with other Git branch strategies, GitHub flow has some highlights and downfalls.

**The Benefits of GitHub Flow**

* Of the three Git branch strategies we cover in this post, GitHub flow is the most simple.
* Because of the simplicity of the workflow, this Git branching strategy allows for Continuous Delivery and Continuous Integration.
* This Git branch strategy works great for small teams and web applications.




**The Challenges of GitHub Flow**

* This Git branch strategy is unable to support multiple versions of code in production at the same time.
* The lack of dedicated development branches makes GitHub flow more susceptible to bugs in production.

## **GitLab Flow Branch Strategy**

At its core, the GitLab flow branching strategy is a clearly-defined workflow. While similar to the GitHub flow branch strategy, the main differentiator is the addition of environment branches or release branches, depending on the situation.

Just as in the other two Git branch strategies, GitLab flow has a main branch that contains code that is ready to be deployed. However, this code is not the source of truth for releases.

In GitLab flow, the feature branch contains work for new features and bug fixes which will be merged back into the main branch when they’re finished, reviewed, and approved.

**Using GitLab flow in your release cycle**

The GitLab flow branching strategy works with two different types of release cycles:

**1. Versioned Release:** each release has an associated release branch that is based off the main branch. Bug fixes should be merged into the main branch first, before being cherry-picked into the release branch.

**1. Continuous Release:** production branches are utilized to contain deployment-ready code, so code is merged into the production branch when it’s ready to be released.

**Benefits of GitLab Flow**

When compared to the Git flow branch strategy, GitLab flow is more simple.
GitLab flow is more organized and structured than the GitHub flow branch strategy.
After slight modification, GitLab flow can allow for Continuous Delivery and versioned releases.



**Challenges of GitLab Flow**

GitLab flow is not the simplest Git branch strategy.
GitLab flow is not the most structured Git branching strategy which can lead to messy collaboration.



---
<br>
    
# **Bibliography**
    
https://www.git-tower.com/learn/git/commands/git-commit
https://www.simplilearn.com/tutorials/git-tutorial/what-is-git
https://blog.testproject.io/2021/03/22/git-commands-every-sdet-should-know/
https://devconnected.com/how-to-create-git-tags/
https://rogerdudler.github.io/git-guide/index.es.html
https://www.atlassian.com/es/git/tutorials/saving-changes/git-stash#:~:text=El%20comando%20git%20stash%20almacena,aplicar%20los%20cambios%20m%C3%A1s%20tarde.
https://www.atlassian.com/git/tutorials/git-hooks
https://www.freecodecamp.org/espanol/news/la-guia-definitiva-para-git-merge-y-git-rebase/
https://www.solucionex.com/blog/git-merge-o-git-rebase
https://www.gitkraken.com/learn/git/best-practices/git-branch-strategy
https://www.git-tower.com/learn/git/faq/git-squash


