# Making `alias` commands for the Terminal

[Tutorial](https://linuxize.com/post/how-to-create-bash-aliases/)

An alias is a shortcut that you can use in the Terminal window for commands that you use often.

You have already seen the `ll` alias for `ls -alF`.

Aliases are stored in a hidden `.bashrc` file in your Home directory. Open this file in VS Code, and skim through its contents:

```bash
code ~/.bashrc
```

You will see that it contains standard settings for the way the Terminal window should behave. To create new aliases, you will need to edit this file. Around line 90, you might find a section like this:

```bash
# some more ls aliases
alias ll='ls -alF'
alias la='ls -A'
alias l='ls -CF'
```
This is where the `ll` alias is defined. You can use `man ls` to see what the -A, -C and -F flags do.

## Exercise

**Customize your `.bashrc` file, so that it you can use aliases to speed up your development process.**

1. Run the command `code ~/.bashrc`
2. Scroll to the end
3. Insert an alias to open this file automatically, for when you want to add a new alias:
    ```bash

    #—————————————————— Add new aliases above this line ——————————————————#

    ## Shortcut to open this file in an editor window
    alias addalias='code ~/.bashrc'
    ## Now run `source ~/.bashrc` in the Terminal to activate your new alias
    ```
4. Note that your new alias will not automatically become available until you start a new Terminal session. You can refresh your source of aliases by typing the following in the Terminal window:
    ```bash
    source ~/.bashrc
    ```
5. The shortcut `git commit -am` is of limited use. It will not add new files to the staging area, and it will not let you use VS Code to create the commit message. And it is also quite a long command to type. You can create an alias for a command that will tell git to automatically add all changed files to the staging area, and then prepare a commit message in the VS Code editor.<br><br>Create a space above the lines that you have just added, and insert a new alias:
    ```bash
    # Automatically add all changed files and open an editor for the commit message
    alias gmit='git add .;git commit'
    ```

6. Note that it is useful:
   * To use a name that is meaningful. This is a shortcut for a command that starts with **g**it and ends with com**mit**. (You can choose your own alias name if you have a better idea).
   * To include a comment to explain what your alias does, so that you can remind yourself about it later.

7. Create an alias that will `cd` to the directory that contains your `.git` folder, at the root of your project.
    ```bash
    # cd to the top-level directory of the current git project
    # (where the .git folder is stored)
    alias gd='cd $(git rev-parse --show-toplevel)'
    ```
8. You can also create functions that you can call from anywhere. Functions can take parameters. The following `mkcd` function combines a `mkdir` command with a `cd`-into-the-new-directory command. The name of the directory to create is passed as a parameter, exactly like for the `mkdir`command.

    ```bash
    # Create a new directory then cd into it.
    # Notes:
    # * The `$1` variable refers to the first parameter of the command.
    #   For example, if you run the command `mkcd myProject`, the $1
    #   variable will contain the string 'myProject'
    # * The end of the flags is indicated by `--`. This means that you
    #   can create a directory whose name starts with a hyphen, and the
    #   directory name will not be treated as a flag.
    mkcd () {
      mkdir -p -- "$1" && cd -P -- "$1"
    }
    ```
9. Here's a function that can be useful when debugging a Git project. If you run `gits` from inside a project directory, it will output the path to the root folder, where the invisible `.git` directory is stored. If you have, by mistake, created your project inside another directory that is already part of another Git project, it will warn you that you have multiple `.git` folders present.
    ```bash
    # Use the gits function to echo the location of all .git directories
    # in the working directory or any of its parent directories. If more
    # than one .git directory is found, you must correct this error.
    gits () {
        found=0     # count the number of times a .git directory is found
        folder=.git # folder to look for
        path=$(pwd) # start from the current working directory

        while [[ "$path" != "" ]]; do
            if [ -e "$path/$folder" ]
            then
                # There is a .git folder in the directory defined by $path
                let found+=1
                echo $folder folder found at $path
            fi
            path=${path%/*} # remove the last directory name from $path
        done

        if [ $found -eq 0 ]
        then
            echo No $folder folder found
        elif [ $found -gt 1 ]
        then
            echo $found $folder folders found. Please correct this.
        fi
    }
    ```
10. Finally (for now), here is a shortcut that will be useful when you start customizing your settings for VS Code.
    ```bash
    # Shortcut to open a new window showing the directory containing user
    # settings
    alias user='code ~/.config/Code/User/'
    ```

## Share your `alias`es

If you create new `alias`es that you think others will find useful, please fork this repository and create a Pull Request to add your contributions to the (visible) `bashrc` file in the same folder as this article. Thanks in advance!
