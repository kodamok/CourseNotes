# Merge conflicts
If two collaborators both make changes in the same place in the same file, it is not possible to merge automatically. Imagine this original file:
```md
# Original Version

* List
* with
* bullet
* points
```
* A collaborator talks to the client and changes this to:
```md
# Client-approved Header

* List
* with
* bullet
* points
```
* Meanwhile, the original developer realizes that "Version" should be "Header" and that a numbered list is better than a bullet list:
```md
# Original Header

1. List
1. with
1. numbered
1. items
```
* When the collaborater pushes changes to a branch called `client-signoff` to their fork, it is clear that there is a conflict:
![Can't merge automatically](img/conflict.png)
You can create a Pull Request, but the Merge Pull Request button will be disabled.
![No merge button](img/no_merge_button.png)
* You must follow the command line instructions:
* `git checkout -b DCIForks-client-signoff main`
* `git pull https://github.com/DCIForks/merge-conflict.git client-signoff`
* The "merged" file will contain both versions
  - Separated by a line of `=======` equals signs
  - With information about the source of each

![Resolve the conflict](img/resolve_conflict.png)
* Select one alternative or the other:
```md
# Client-approved Header

1. List
1. with
1. numbered
1. items
```

* Commit the file that resolves the conflict:
* `git add .`
* `git commit -m "Client-approved Header accepted"`
* `git log`
```bash
commit 7550e24a6fd80ce706803f83b390c8e4a3db2647
Merge: 970e77c 3dfc50c
Author: James Newton <blackslate@lexogram.com>
Date:   Thu Apr 15 00:57:08 2021 +0300

    Client-approved Header accepted

commit 970e77c575666f904fa2709cc41886d727459a37
Author: James Newton <blackslate@lexogram.com>
Date:   Thu Apr 15 00:41:53 2021 +0300

    Modify Header

commit bbfa73cc0ad2d051952c3485a6178ecbf42203c9
Author: James Newton <blackslate@lexogram.com>
Date:   Thu Apr 15 00:40:04 2021 +0300

    Switch to numbered list

commit 3dfc50ce921c1e12c8c75098560d0ee48c448c0a
Author: James Newton <blackslate@lexogram.com>
Date:   Thu Apr 15 00:38:20 2021 +0300

    Client-approved Header

commit 85b9d7408068809ad554c122b76e737dff10f60a
Author: James Newton <blackslate@lexogram.com>
Date:   Thu Apr 15 00:26:55 2021 +0300

    Original version with bullet points
```
