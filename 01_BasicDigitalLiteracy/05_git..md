# `git`

## What is git?
* Version Control System (VCS)
* Created by Linus Torvalds
* Allows you to:
  - Save snapshots of your project as you work
  - Keep a copy of your project in the cloud, so that you can work on it from any computer
  - Revert to a previous version, if you make a mistake
  - Make a `branch`, to try out a new idea, without breaking the current stable version
  - Make a "fork" of another project
    - To collaborate with the project owner
    - To build your own project on the foundation of an existing one
  - Propose changes to the owner of a project (Pull requests)
  - `merge` different branches (successful tests and contributions from others)

## Installation

* Git may already be installed
  - `git --version`
* Using bash to [install Git on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-20-04)
  - `sudo apt update`
  - `sudo apt install git`
  - `git --version`
* On MacOS:
  - [Download the installer](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git#_installing_on_macos)
* On Windows:
  - [Download the installer](https://git-scm.com/download/win)
  - [Follow the instructions](https://phoenixnap.com/kb/how-to-install-git-windows)

## Configure git
Tell git who you are and where to contact you, so that your contributions to other repositories can be credited to (or blamed on) you.
- `git config --global user.name "Your Name"`
- `git config --global user.email "your_email@domain.com"`

* [Set VS Code to be default editor for `commit`](https://stackoverflow.com/a/36644561/1927589)
  * Check `code --help` works
  * (See [Stack Overflow answer](https://stackoverflow.com/a/36644561/1927589) if not)
  * `git config --global core.editor "code --wait"`

## Introduction: git Version Control Systems (VCS)
* Initializing:
  - The `git` program
  - Starting a repository with `git init`
  - The `.git` folder

* Basic workflow:
  - Checking the status with `git status`
  - Staging files with `git add`
  - Using the `.` shortcut to add all files
  - Creating a commit with `git commit`
  - Viewing the history with `git log`
  - Quick commits with `git commit -am <message>`

* Branching:
  - Moving through the history with `git checkout <commit hash>`
  - Branching out with `git checkout -b <branch name>`
  - Viewing branches with `git branch`
  - Merging with `git merge`
