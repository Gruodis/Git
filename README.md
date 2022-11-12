<p align="center"><img width="150" alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://www.biteinteractive.com/wp-content/uploads/2021/05/git-vs-github.png"></p>

<h1 align="center">
# Git & Github 101
 </h1>

## Git:
  - [Basics](#here-are-some-common-commands-for-using-git)
  - [Example: Start new repo and publish to GitHub](#example-start-a-new-repository-and-publish-it-to-github)
  - [Example: Contribute to an existing repo](#example-contribute-to-an-existing-repository)
    - [Final Steps MySQL](#computer-mysql-setup-final-step-securing-mysql)
  - [If Composer & MySQL Installed](#computer-if-composer--mysql-installed)
  - [Start Project](#computer-start-existing-project)
  - [If something fails](#bangbang-if-project-doesnt-start-properly-try)

### Here are some common commands for using Git:

-  ``git init`` initializes a brand new Git repository and begins tracking an existing directory. It adds a hidden subfolder within the existing directory that houses the internal data structure required for version control.

-  ``git clone`` creates a local copy of a project that already exists remotely. The clone includes all the project's files, history, and branches.

-  ``git add`` stages a change. Git tracks changes to a developer's codebase, but it's necessary to stage and take a snapshot of the changes to include them in the project's history. This command performs staging, the first part of that two-step process. Any changes that are staged will become a part of the next snapshot and a part of the project's history. Staging and committing separately gives developers complete control over the history of their project without changing how they code and work.

-  ``git commit`` saves the snapshot to the project history and completes the change-tracking process. In short, a commit functions like taking a photo. Anything that's been staged with ``git add`` will become a part of the snapshot with ``git commit``.

-  ``git status`` shows the status of changes as untracked, modified, or staged.

-  ``git branch`` shows the branches being worked on locally.

-  ``git merge`` merges lines of development together. This command is typically used to combine changes made on two distinct branches. For example, a developer would merge when they want to combine changes from a feature branch into the main branch for deployment.

-  ``git pull`` updates the local line of development with updates from its remote counterpart. Developers use this command if a teammate has made commits to a branch on a remote, and they would like to reflect those changes in their local environment.

-  ``git push`` updates the remote repository with any commits made locally to a branch.

<hr/>

### Example: Start a new repository and publish it to GitHub

- ```
  # create a new directory, and initialize it with git-specific functions
  git init my-repo

  # change into the `my-repo` directory
  cd my-repo

  # create the first file in the project
  touch README.md

  # git isn't aware of the file, stage it
  git add README.md

  # take a snapshot of the staging area
  git commit -m "add README to initial commit"

  # provide the path for the repository you created on github
  git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git

  # push changes to github
  git push --set-upstream origin main
  ```

<hr/>

### Example: Contribute to an existing repository
- ```bash
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

<hr/>

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

<hr/>

### Commit local project to github repo:

   - ```bash
     git init git add .    (add all files to stage for later commit)git commit -m "Message to describe commit."
     ```
-  pull request update project - patikriname ar nėra branch'e pasikeitimų
-  jeigu commit metu failas neisikelia i serveri ir raudonuoja, reikia Git -> Add (įkeliam failą į stage).

-  Merge your branch into **develop** (No Pull request needed)
-  Create Pull request into **master** branch
-  **TEST your feature in staging server**


<hr/>
