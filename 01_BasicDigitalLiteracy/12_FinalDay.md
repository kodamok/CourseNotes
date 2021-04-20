# Points covered in the Basic Digital Literacy module

## Virtual Studio Code

* [Install](https://code.visualstudio.com/download)
* [Quick Start Guide](https://docs.microsoft.com/en-us/visualstudio/liveshare/quickstart/join)

### Add extensions
* [Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-pack)
* [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
* [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)

---
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
### Documentation
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
* `git config --global user.name "Your Name"`
* `git config --global user.email "youremail@domain.com"`
* `git config --global core.editor "code --wait"`
* [Create SSH public key for GitHub](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)
* [GitHub Student Developer Pack](https://gist.github.com/LeandroDCI/b9f53690be5f2aaef2e93913bab5ff13)

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
```bash
git remote add origin git@github.com:<account_name>/<repo_name>.git
git branch -M main
git push -u origin main
```

### Forking a repository

* Visit source project repository
* Click on Fork
* Select your person GitHub account

### Cloning a repository from GitHub to your local computer
* In your browser;
  * Visit the repository page on GitHub
  * Open the <> Code tab
  * Click on the green Code button
  * Copy the SSH url for the repository
* In VS Code, on your local computer
  * Open a new window
  * Open (create) a directory for the project
  * Open the Terminal pane
  * `cd` into the project directory
  * Paste the copied lines of bash code, and execute them

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

### [Issues](https://guides.github.com/features/issues/)
* In the GitHub repository page, visit the Issues tab
* Click on New Issue
* Enter a title
* Describe the issue, using MarkDown
* Select one or more labels (edit the label list as needed)
* Click Submit New Issue
* Check the Filters drop-down menu
* [Link Pull Requests to Issues](https://docs.github.com/en/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue)


---

## Unix, Linux and Ubuntu and the WWWeb

* For Linux, what are the kernel and the shell?
* Who developed Linux and git?
* [Resources](https://github.com/DigitalCareerInstitute/web-dev-v3-curriculum/tree/master/1_Basic-Digital-Literacy/1.2_Web-Dev)

## [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Group Dynamics
* Group name
* Group logo

---
---

# Tests

* [BDL Assessment Basic (bash)](https://forms.gle/4YHiFaJEVon77vL99)
  60 minutes: 11:00 - 12:00
* [BDL Assessment Git/GitHub)](https://forms.gle/QvX4iLnaDfX8JhkR7)
  60 minutes: 15:00 - 16:00
