# Points covered in this module

## bash
* What is bash?
* What operating systems does it work on?

### Basic commands in the Terminal
* cd
* clear
* cp
* echo
* ll
* ls (-alF)
* mkdir (-p)
* mv
* pwd
* reboot
* rm
* rmdir (-rf)
* sudo
* touch
* whereis
* which
* whoami
---
* --help
* man
### Parameters
* -flags
* arguments
### [Operators](https://unix.stackexchange.com/a/159514)
* ;
* &&
* |
* \# (comment)
* \>>
### Folder shortcuts
* .
* ..
* ~
* -
* /
### Text
* less
* head
* tail
* nano
* pico
---
### Productivity shortcuts
* [Cheat Sheet](https://gist.github.com/tuxfight3r/60051ac67c5f0445efee)
* alias
* code

keyboard|effect
-|-
up  and down arrows|history
left  and right arrows|move insertion cursor
tab|autocomplete
Ctrl-A|move to beginning of line
Ctrl-C|cancel current command
Ctrl-Shift-C|Copy
Ctrl-Shift-V|Paste
Ctrl-left_arrow|back one word
Alt-(Shift-)B|back one word
Alt- Shift- F|forward one word
Ctrl-right_arrow|forward one word
Ctrl-xx|Toggle between start of line and current cursor position
ctrl-], x|Where x is any character, moves the cursor forward to the next occurence of x
Ctrl-L|clear the Terminal
---
### Coming soon: more productivity tips
* alias
* [Keyboard shortcuts for VS Code](https://blog.logrocket.com/learn-these-keyboard-shortcuts-to-become-a-vs-code-ninja/)
* Snippets

## [Packages and package managers](https://itsfoss.com/package-manager/)
* What is a package?
* Examples:
  - curl (Client URL)
  - nvm  (Node Version Manager)
  - tree

### Using the [`apt` package manager](https://itsfoss.com/apt-command-guide/)
* Installs programs and applications, and keeps them up-to-date
* Need for `sudo` admin privileges for installations and removals
---
* `apt list --installed`
---
* `sudo apt update`
* `sudo apt upgrade`
* `sudo apt full-upgrade`
* `-y` flag = answer all questions with Yes automatically
* `sudo apt update && sudo apt upgrade -y`
---
* `apt show` \<package>
* `sudo apt install` \<package>
---
* `sudo apt remove` \<package>
* `sudo apt purge` \<package> #also removes configuration files
* `sudo apt autoremove`

### Using `nvm` to install Node.js
* What does Node Version Manager do?
* Use `apt` to [install NVM](https://www.cyberithub.com/install-nvm-for-node-js-on-ubuntu-20-04/)
* `nvm install node`

### Using `npm` to [install](https://docs.npmjs.com/cli/v7/commands/npm-install) Node modules
* `npm install `\<module>
or
* `npm i `\<module>
* Example: `npm install -g [sass](https://sass-lang.com/)`
---
## git and GitHub

### [Install](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-20-04) and configure Git

* `sudo apt update`
* `sudo apt install git`

### Creating a repository locally
* `cd `path/to/parent/directory
* `mkdir `projectName
* `cd `projectName
* `git init`
* `tree -a` # to see the newly created invisible .git directory and its contents

### Creating a snapshot of your project
* Make changes
* `git status` # to see what files have been added, changed or deleted
* `git diff` # to see what lines have been  added, changed or deleted in modified files
* Press space bar to show more `diff` information
* Press Shift-Q to exit the `diff` program
* `git add .`
* `git commit`

### Linking a local repository to a remote repository on GitHub
* Create an account on GitHub
* Visit your repository page
* Click on the New button to create a new repository on GitHub
* DO NOT add any files (no README file, no .gitignore, no licence files)
* Click on Create Repository
* Copy the 3 lines:

### Forking a repository

### Cloning a repository from GitHub to your local computer

### Working with branches
* `git branch`
* `git branch -v`
* `git branch newBranchName`
* `git checkout existingBranchName`
* `git branch -b new_branch_name`
* `git branch --delete nameOfBranchToDelete`
* `git branch -d nameOfBranchToDelete`

### Pull Requests
* Fork the project repository on GitHub
* Clone your fork to your local computer
* Create a branch with a change-specific name
* Make your changes
* Commit your changes
* Push your change-specific branch to your GitHub repository
* Visit you GitHub repository page
* Select the Pull Requests tab
* Click on the Compare & Pull Request button
* Enter any additional information
* Click on Create Pull Request

### Merging branches
* Pull collaborator's branch from GitHub, if necessary
* `git checkout `\nameOfRecipientBranch
* `git merge `\nameOfSourceBranch
* Resolve any conflicts
  - Find lines with `<<<<<<< ======= >>>>>>>`
  - Decide which conflicting lines to keep, which to delete, which to change
  - Remove the lines with `<<<<<<< ======= >>>>>>>`
  - Commit the changes
* Abort merge using `git merge --abort`

### Synchronizing with upstream repository
On your local copy of your fork:
* `git checkout main`
* `git pull upstream/main`

### Issues


---

## Unix, Linux and Ubuntu

* For Linux, what are the kernel and the shell?
* Who developed Linux and git?

## The structure of the web

## [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

---
---

# Tests

* [BDL Assessment Basic (bash)](https://forms.gle/4YHiFaJEVon77vL99)
  60 minutes: 11:00 - 12:00
* [BDL Assessment Git/GitHub)](https://forms.gle/QvX4iLnaDfX8JhkR7)
  60 minutes: 15:00 - 16:00
