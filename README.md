> **Instructions**
> 
> 1. Read Chapters 2 & 3 of [Pro Git][ProGit]. The chapters are short.
> 2. Answer these questions using [Markdown format][markdown-cheatsheet] (also [Github Markdown][github-markdown]). 
> 3. Place your answers between lines beginning with 3 backquotes, which tells Markdown it should be unformatted text, and write only the commands you would type (**no** shell prompt).
>    Indent the 3 backquotes so they line up with the question text (3 leading spaces) so Markdown formats you answer as part of the numbered item.
>    Example:
>    ```
>    git init
>    ```  
> 4. **Test that your answers are correct!** There is **no excuse** for incorrect answers since you can test your answers by experimentation.      
> 5. **Delete these instructions and all "TODO" lines.** Points deducted for each "TODO" in submitted work.   
> 6. Verify that your Markdown formatting is correct -- points deducted for bad formatting. VS Code and IntelliJ have markdown previewers. You should also preview it on Github, since Github Markdown is a bit non-standard.
>   *Excellent VS Code Markdown Previewer*: the [Markdown Preview Enhanced][vscode-markdown-preview-enhanced] extension.

## Using Git

> TODO: Create a table of contents here.  Each line should be a clickable link to each part of this document or another file containing the questions and answers. One item per line.

[Basics](#basics)    
[Adding and Changing Things](#adding-and-changing-things)    
[Next Section (todo: Fix This)](#next-section)    
[Next Section (todo: Fix This)](#next-next-section)    
[Commands for Remotes](remote-commands.md)   
[Favorites](#favorites)     
[Resources](#resources)

#### Note on Paths

In this file, directory paths are written with a forward slash as on MacOS, Linux, and the Windows-Bash shell: `/dir1/dir2/somefile`.    


## Basics

1. When using Git locally, what are these?  Define each one in a sentence
   * Staging area -
   * Working copy -
   * master -
   * HEAD -

2. When you install git on a new machine (or in a new user account) you should perform these 2 git commands to tell git your name and email.  These values are used in commits that you make:
   ```
   # Git configuration commands for a new account


   ```

3. There are 2 ways to create a local Git repository.  What are they?
   - todo: briefly describe first way
   - todo: briefly describe second way

4. When you create a git repository by entering `git init`, Git will create a "hidden" directory for the local repository.  Where is the directory for this local repository (relative to the directory where you typed "git init")?



## Adding and Changing Things

Suppose your working copy of a repository contains these files and directories:
```
README.md
out/
    a.exe
src/a.py
    b.py
    c.py
test/
    test_a.py
    ...
```     
> TODO: Write the git command to perform each of these:

1. Add README.md and *everything* in the `src` directory to the git staging area.
   ```
   todo  your answer here
   ```

2. Add `test/test_a.py` to the staging area (but not any other files).
   ```
   todo  your answer here
   ```

3. List the files in the staging area.


4. Remove `README.md` from the staging area. (Useful if you accidentally add something you don't want to commit.)


5. Commit everything in the staging area to the repository.


6. Describe 2 steps to configure the repository so git will ignore all files in the `out/` directory:
   - step one
   - step two

7. Command to move all the .py files from `src` to the top-level directory of this repository, so they are also moved in the Git repo.


8. Commit this change with the message "moved src directory":


9. Command to add **all changed files** (but not untracked files) to the staging area using a single command.


10. **Delete** the file `c.py` from your working copy **and** the repository:



## Undo Changes and Recover Files

> TODO: enter the git command to do each of these

1.  Display the differences between your *working copy* of `a.py` and the `a.py` in the *local repository* (HEAD revision):

2. Display the differences between your *working copy* of `a.py` and the version in the *staging area*. (But, if a.py is not in the staging area this will compare working copy to HEAD revision):

3. **View changes to be committed:** Display the differences between files in the staging area and the versions in the repository. (You can also specify a file name to compare just one file.) 


4. **Undo "git add":** If `main.py` has been added to the staging area (`git add main.py`), remove it from the staging area:


5. **Recover a file:** Command to replace your working copy of `a.py` with the most recent (HEAD) version in the repository.  This also works if you have deleted your working copy of this file.


6. **Undo a commit:** Suppose you want to discard some commit(s) and move both HEAD and "master" to an earlier revision (an earlier commit)  Suppose the git commit graph looks like this (`aaaa`, etc, are the commit ids)
   ```
   aaaa ---> bbbb ---> cccc ---> dddd [HEAD -> master]
   ``` 
   The command to reset HEAD and master to the commit id `bbbb`:


7. **Checkout old code:** Using the above example, the command to replace your working copy with the files from commit with id `aaaa`:
   ```
   todo your answer here
   ```
    Note:
    - Git won't let you do this if you have uncommitted changes to any "tracked" files.
    - Untracked files are ignored, so after doing this command they will still be in your working copy.
 

## Viewing Commits

1. Show the history of commits, using one line per commit:
   ```
   git log --oneline
   ```
   Some versions of git have an *alias* "log1" for this (`git log1`).

2. Show the history (as above) including *all* branches in the repository and include a graph connecting the commits:


3. List all the files in the current branch of the repository:
   ```
   todo your answer
   ```
   example output:
   ```
   .gitignore
   README.md
   a.py
   b.py
   test/test_a.py
   test/test_b.py
   ```


## Branch and Merge

> TODO write the commands to do each of these
1. Create a new branch named `dev-foo`:
 
2. Display the name of your current branch:

3. List the names of **all** branches, including remote branches:

4. Switch your working copy to the branch named `dev-foo`:

5. **Merge:** To merge the work from `dev-foo` into the master branch, perform these steps:
   > TODO: write a description of the steps and the git command(s) for each step
   1. step one
      ```
      git do something
      ```
   2. step two
      ```
      git do something else
      ```


6. Describe under what conditions a merge may fail.




## Favorites

> TODO: Add *at least* 1 git task that (a) that you'd like to remember, or (b) you think is really useful, and the git command(s) to do it.



---
## Resources

> TODO: Add your favorite Git resources (at least 1)

[Pro Git Online Book][ProGit] Chapters 2 & 3 contain the essentials. Downloadable PDF is also available.     
[Visual Git Reference](https://marklodato.github.io/visual-git-guide) one page with illustrations of git commands.

Try Git:

[Learn Git Interactive Tutorial][LearnGitInteractive] excellent visual tutorial.   
[Git Visualizer][VisualizeGit] execute Git commands in a web browser and see the results as a graph.    

[ProGit]: https://www.git-scm.com/book/en/v2 "Pro Git online book on Git-scm.com"
[ProGitPdf]: https://progit2.s3.amazonaws.com/en/2016-03-22-f3531/progit-en.1084.pdf "Pro Git v.2 PDF on AWS. Longer, book format."
[LearnGitInteractive]: https://learngitbranching.js.org "Interactive graphical git tutorial"
[VisualizeGit]: http://git-school.github.io/visualizing-git/ "Online tools draws a graph of commits in a repo as you type"
[markdown-cheatsheet]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[github-markdown]: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
[vscode-markdown-preview-enhanced]: https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced
