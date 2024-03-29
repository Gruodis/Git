<p align="center"><img width="150" alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://git-scm.com/images/logos/downloads/Git-Logo-White.svg"></p>

<h1 align="center">Git 101</h1>

Git & GitHub Must Know [101](https://www.atlassian.com/git/tutorials/setting-up-a-repository) [#link 1](https://dev.to/juni/git-and-github---must-know-commands-to-make-your-first-commit-333c)
[#link 2](https://learn.microsoft.com/en-us/training/modules/intro-to-git/2-exercise-configure-git)

## Git:
  - [Basics](#here-are-some-common-commands-for-using-git)
  - [Example: Start new repo and publish to GitHub](#example-start-a-new-repository-and-publish-it-to-github)
  - [Example: Contribute to an existing repo](#example-contribute-to-an-existing-repository)
  - [Example: Contribute to an existing branch on GitHub](#example-contribute-to-an-existing-branch-on-github)
  - [Example: Connect a local repository with a remote repository](#connect-local-repo-with-remote)
  - [To check merged branches](#to-check-if-all-branches-merged-in-to-main)
<!--   - [If Composer & MySQL Installed](#computer-if-composer--mysql-installed)
  - [Start Project](#computer-start-existing-project)
  - [If something fails](#bangbang-if-project-doesnt-start-properly-try)
 -->
 
<br />
<hr/>
<br />
<br />


### Here are some common commands for using Git:

-  ``git init`` initializes a brand new Git repository and begins tracking an existing directory.

-  ``git clone`` creates a local copy of a project that already exists remotely.

-  ``git add`` stages a change. This command performs staging, the first part of that two-step process.

-  ``git commit`` saves the snapshot to the project history and completes the change-tracking process. In short, a commit functions like taking a photo. Anything that's been staged with ``git add`` will become a part of the snapshot with ``git commit``.

-  ``git status`` shows the status of changes as untracked, modified, or staged.

-  ``git branch`` shows the branches being worked on locally.

    -  ``git branch -a`` list all branches.
    -  ``git branch -m example-branch`` rename the current branch to example-branch.
    -  ``git branch -d example-branch`` delete example-branch. This is a “safe” operation in that Git prevents you from deleting the branch if it has unmerged changes.
    -  ``git checkout -b branch-name`` Create a branch and checkout in one command.

-  ``git merge`` merges lines of development together. This command is typically used to combine changes made on two distinct branches.

-  ``git pull`` updates the local line of development with updates from its remote counterpart.

-  ``git push`` updates the remote repository with any commits made locally to a branch.

-  ``git checkout branch-name``  switch to a branch.

<hr/>
<br />
<br />
<br />

### Example: Start a new repository and publish it to GitHub

  create a new directory, and initialize it with git-specific functions
  ```bash
  git init my-repo
  ```

  change into the `my-repo` directory
  ```bash
  cd my-repo
  ```

  create the first file in the project
  ```bash
  touch README.md
  ```

  git isn't aware of the file, stage it
  ```bash
  git add README.md
  ```

  take a snapshot of the staging area
  ```bash
  git commit -m "add README to initial commit"
  ```

  provide the path for the repository you created on github
  ```bash
  git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git
  ```

  push changes to github
  ```bash
  git push --set-upstream origin main(master)
  ```
    
<br />
<hr/>
<br />
<br />

### Example: Contribute to an existing repository

  ```bash
  # download a repository on GitHub to our machine
  # Replace `owner/repo` with the owner and name of the repository to clone
  git clone https://github.com/owner/repo.git

  # change into the `repo` directory
  cd repo

  # create a new branch to store any new changes
  git branch my-branch

  # switch to that branch (line of development)
  git checkout my-branch

  # make changes, for example, edit `file1.md` and `file2.md` using the text editor

  # stage the changed files
  git add file1.md file2.md

  # take a snapshot of the staging area (anything that's been added)
  git commit -m "my snapshot"

  # push changes to github
  git push --set-upstream origin my-branch
  ```
  
<br />
<hr/>
<br />
<br />

### Example: contribute to an existing branch on GitHub
This example assumes that you already have a project called repo on the machine and that a new branch has been pushed to GitHub since the last time changes were made locally.

```bash
# change into the `repo` directory
cd repo

# update all remote tracking branches, and the currently checked out branch
git pull

# change into the existing branch called `feature-a`
git checkout feature-a

# make changes, for example, edit `file1.md` using the text editor

# stage the changed file
git add file1.md

# take a snapshot of the staging area
git commit -m "edit file1"

# push changes to github
git push
```

<br />
<hr/>
<br />
<br />

### Commit local project to github repo:

   - ```bash
     git init git add .    (add all files to stage for later commit)git commit -m "Message to describe commit."
     ```
-  pull request update project - patikriname ar nėra branch'e pasikeitimų
-  jeigu commit metu failas neisikelia i serveri ir raudonuoja, reikia Git -> Add (įkeliam failą į stage).

-  Merge your branch into **develop** (No Pull request needed)
-  Create Pull request into **master** branch
-  **TEST your feature in staging server**

<br />
<hr/>
<br />
<br />

### Connect local repo with remote

```bash
git remote add origin <remote_repo_URL>
git push --all origin main(master)
```

If you want to set all of your branches to automatically use this remote repository, then use ``git pull`` , add ``--set-upstream`` to the push:
```bash
git push --all --set-upstream origin main(master)
```
<br />
<hr/>
<br />
<br />

### To check if all branches merged in to main

- Click on "branches"

<br />
<br />

![image](https://github.com/Gruodis/Git/assets/43164261/de348efc-68b5-41df-b1f4-9bf9b16f2911)

