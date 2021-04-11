# [GitHub](https://github.com)
## The [Github website](https://github.com)
  - Create an account
  - Join the FbW-E04-1 Organization and team "All"

## [GitHub Student Developer Pack](https://gist.github.com/LeandroDCI/b9f53690be5f2aaef2e93913bab5ff13 )
  * LOG OUT OF GITHUB before clicking on your link

## Connect to GitHub with SSH
  * [What is SSH?](https://searchsecurity.techtarget.com/definition/Secure-Shell)
  * Why use it?
    * You will be connecting to GitHub to upload files
    * GitHub wants to verify your ID to see if you have access privileges
      - Private repos
      - Organizations
      - Teams
    * Question: how to connect securely to GitHub without entering a password every time.
    * Answer: Use [Public Key (and Private Key) Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)

## [Create a Public Key](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)


## Creating a repository on GitHub
  * Go to your Profile page
  * Click on the tab Repositories
  * Click on the green New button
  * Enter a repository name (include your initials so forks can be identified)
  * Leave the checkboxes unchecked for now ()
  * **Note: *This will set `main` as the default branch.***
  * Click the green Create Repository button

---

  ### Quick setup — if you’ve done this kind of thing before

  * HTTP:
  ```bash
  git clone https://github.com/<your_username>/<your_repo_name>.git
  ```
  or
  * **SSH**
  ```bash
  git clone git@github.com:<your_username>/<your_repo_name>.git
  ```


  Get started by [creating a new file](https://github.com/<your_username>/<your_repo_name>/new/main) or [uploading an existing file](https://github.com/<your_username>/<your_repo_name>/upload). We recommend every repository include a [README](), [LICENSE](), and [.gitignore]().

  …or create a new repository on the command line
  ```bash
  echo "# <Your_repo_name>" >> README.md
  git init
  git add README.md
  git commit -m "first commit"
  git branch -M main
  git remote add origin git@github.com:<your_username>/<your_repo_name>.git
  git push -u origin main
  ```
  …or `push` an existing repository from the command line
  ```bash
  git remote add origin git@github.com:<your_username>/<your_repo_name>.git
  git branch -M main
  git push -u origin main
  ```
  …or import code from another repository

  You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

---

## Cloning, Pushing and Pulling:
- Cloning a remote: `git clone <url>`
- Pushing changes: `git push`
- Pulling changes: `git pull`

## Locals and Remotes:
- Local repository vs. Remote repository
- Checking a repository's remotes: `git remote -v`
- Removing a remote: `git remote remove <name>`
- Adding a remote: `git remote add <name> <url>`
- Pushing a branch for the first time:
  `git push -u <remote name>
  <branch name>`

# Working together with git and GitHub

## Forks

## Conflicts:
  - Making changes to the same file in the same branch
  - Resolving pull conflicts (with VS Code / Atom)
  - Minimizing conflicts: Single branch per person per task (GitHub Flow)

## Reviewing:
  - Creating a Pull Request on GitHub
  - Pull Request review process
  - Dealing with conflicts in Pull Request (Test merging)
  - Merging on GitHub


# BDL test
* git
* Github
* markdown
* commit etiquette
* pull request
* pull / push
* merge
* clone = master branch only?
