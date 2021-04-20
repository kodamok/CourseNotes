# Use `mkdir` to create a folder structure for a site
* `mkdir -p site/css # creates parent folders as needed`
* `mkdir site/js`

# Install the `tree` program
* `sudo apt-get update`
* `sudo apt-get install tree`

* `tree`
```bash
.
└── site
    └── css
```

# Create empty files
* `touch site/index.html site/css/styles.css`
* `tree`
```bash
.
└── site
    ├── css
    │   └── styles.css
    └── index.html
```

# Start tracking changes with `git`
* `cd site`
* `git init`
* `tree -a`
```bash
.
├── css
│   └── styles.css
├── .git
│   ├── branches
│   ├── config
│   ├── description
│   ├── HEAD
│   ├── hooks
│   │   ├── applypatch-msg.sample
│   │   ├── commit-msg.sample
│   │   ├── post-update.sample
│   │   ├── pre-applypatch.sample
│   │   ├── pre-commit.sample
│   │   ├── prepare-commit-msg.sample
│   │   ├── pre-push.sample
│   │   ├── pre-rebase.sample
│   │   └── update.sample
│   ├── info
│   │   └── exclude
│   ├── objects
│   │   ├── info
│   │   └── pack
│   └── refs
│       ├── heads
│       └── tags
└── index.html
```

# Tell git to record a snapshot of the project
* `git add .`
* `git commit -m "Basic folder structure"`
```bash
[master (root-commit) 0d45724] Basic folder structure
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 css/styles.css
 create mode 100644 index.html
```
* `git log`
```bash
commit 0d457240f1016213f6e5bab7289398bd31250c9c
Author: James Newton <blackslate@lexogram.com>
Date:   Mon Apr 12 23:12:36 2021 +0300

    Basic folder structure
```
# Edit the html and css files in VS Code
* File > Open Folder
* Select the site/ folder
* Edit the `index.html` and `css/styles.css` files
* `git diff`
```bash
diff --git a/css/styles.css b/css/styles.css
index e69de29..3c27d62 100644
--- a/css/styles.css
+++ b/css/styles.css
@@ -0,0 +1,4 @@
+h1 {
+  background-color: black;
+  color: white;
+}
diff --git a/index.html b/index.html
index e69de29..80fb64e 100644
--- a/index.html
+++ b/index.html
@@ -0,0 +1,14 @@
+<!DOCTYPE html>
+<html lang=en>
+<head>
+  <meta charset="utf-8">
+  <title>Site</title>
+  <link rel="stylesheet" href="css/styles.css" />
+</head>
+<body>
+<h1>Site</h1>
+<p>
+  This site is online!
+</p>
+</body>
+</html>
```
* `git status`
```bash
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   css/styles.css
	modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
```

# Commit the changes
* `git add .`
* `git commit -m "Update index.html and css/styles.css"`
* `git log`
```bash
commit 26f9a28998117886cb130ef59ca44b689bda229e
Author: James Newton <blackslate@lexogram.com>
Date:   Mon Apr 12 23:25:15 2021 +0300

    Update index.html and css/styles.css

commit 0d457240f1016213f6e5bab7289398bd31250c9c
Author: James Newton <blackslate@lexogram.com>
Date:   Mon Apr 12 23:12:36 2021 +0300

    Basic folder structure
```

# Change the CSS for the worse
* `git diff`
```bash
diff --git a/css/styles.css b/css/styles.css
index 3c27d62..40f080f 100644
--- a/css/styles.css
+++ b/css/styles.css
@@ -1,4 +1,4 @@
 h1 {
-  background-color: black;
-  color: white;
+  background-color: purple;
+  color: orange;
 }
```
* `git status`
```bash
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   css/styles.css

no changes added to commit (use "git add" and/or "git commit -a")
```
* `git add .`
* `git commit -m "Bad design choice"`
``` bash
[master ec59808] Bad design choice
 1 file changed, 2 insertions(+), 2 deletions(-)
```

# Return to the previous (acceptable) commit
* `git checkout 26f9a28`
```bash
Note: checking out '26f9a28'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b <new-branch-name>

HEAD is now at 26f9a28... Update index.html and css/styles.css
```
# Create a new branch
* `git checkout -b dev`
or
* `git branch dev`
* `git checkout dev`
```bash
Switched to a new branch 'dev'
```
* `git log`
```bash
commit 26f9a28998117886cb130ef59ca44b689bda229e
Author: James Newton <blackslate@lexogram.com>
Date:   Mon Apr 12 23:25:15 2021 +0300

    Update index.html and css/styles.css

commit 0d457240f1016213f6e5bab7289398bd31250c9c
Author: James Newton <blackslate@lexogram.com>
Date:   Mon Apr 12 23:12:36 2021 +0300

    Basic folder structure
```
* `git branch -v`
```bash
* dev    26f9a28 Update index.html and css/styles.css
  master ec59808 Bad design choice
```

# Return to the `master` branch
* `git checkout master`
```bash
Switched to branch 'master'
```

# Push the repository to GitHub
* `git remote -v`
```
```
* Visit `https://github.com/<your_user_name>`
* Click on Repositories tab
* Click on the green New button
* Fill in the Repository Name field
* Click on Create Repository
```bash
git remote add origin git@github.com:<your_user_name>/<your_repo_name>.git
git branch -M main
git push -u origin main
```
### Use a politically correct branch name
* `git branch -M main`
* `git branch -v`
```bash
  dev  26f9a28 Update index.html and css/styles.css
* main ec59808 Bad design choice
```
* `git remote add origin git@github.com:FbW-E04-1/site-for-sore-eyes.git`
* `git remote -v`
```bash
origin	git@github.com:FbW-E04-1/site-for-sore-eyes.git (fetch)
origin	git@github.com:FbW-E04-1/site-for-sore-eyes.git (push)
```
* `git push -u origin main`
```bash
Counting objects: 13, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (9/9), done.
Writing objects: 100% (13/13), 1.14 KiB | 0 bytes/s, done.
Total 13 (delta 0), reused 0 (delta 0)
To git@github.com:FbW-E04-1/site-for-sore-eyes.git
 * [new branch]      main -> main
Branch main set up to track remote branch main from origin.
```

# Make changes in the `dev` branch
* `git checkout dev`
```bash
Switched to branch 'dev'
```
* `git diff`
```bash
diff --git a/css/styles.css b/css/styles.css
index 3c27d62..e1ecc16 100644
--- a/css/styles.css
+++ b/css/styles.css
@@ -1,3 +1,9 @@
+body {
+  width: 600px;
+  margin: 0 auto;
+  text-align: center;
+}
+
 h1 {
   background-color: black;
   color: white;
```
* `git add .`
* `git commit -m "Centre and limit width"`
```bash
[dev 7fe450e] Centre and limit width
 1 file changed, 6 insertions(+)
```

# `merge` the changes into the main branch
* `git checkout main`
```bash
Switched to branch 'main'
Your branch is up-to-date with 'origin/main'.
```
* `git diff dev`
```bash
diff --git a/css/styles.css b/css/styles.css
index e1ecc16..40f080f 100644
--- a/css/styles.css
+++ b/css/styles.css
@@ -1,10 +1,4 @@
-body {
-  width: 600px;
-  margin: 0 auto;
-  text-align: center;
-}
-
 h1 {
-  background-color: black;
-  color: white;
+  background-color: purple;
+  color: orange;
 }
```
* `git merge dev`

> Merge branch 'dev' into main
>
> \# Please enter a commit message to explain why this merge is necessary
>
> \# especially if it merges an updated upstream into a topic branch.
>
> \#
>
> \# Lines starting with '#' will be ignored, and an empty message aborts
>
> \# the commit.

```bash
Auto-merging css/styles.css
Merge made by the 'recursive' strategy.
 css/styles.css | 6 ++++++
 1 file changed, 6 insertions(+)
```

# Moral: commits are applied in chronological order
