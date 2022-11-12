<p align="center"><img width="150" alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/1280px-Git-logo.svg.png"></p>

<h1 align="center">
# Git & Github 101
 </h1>

## Git:


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

-  Commit local project to github repo:

   - ```bash
     git init git add .    (add all files to stage for later commit)git commit -m "Message to describe commit."
     ```
-  pull request update project - patikriname ar nėra branch'e pasikeitimų
-  jeigu commit metu failas neisikelia i serveri ir raudonuoja, reikia Git -> Add (įkeliam failą į stage).

-  Merge your branch into **develop** (No Pull request needed)
-  Create Pull request into **master** branch
-  **TEST your feature in staging server**


<hr/>
