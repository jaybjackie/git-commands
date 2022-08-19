## Commands for Remotes


1. List all your remote repositories and show their URLs:
   ```
   git remote -v

   origin  https://github.com/jaybjackie/git-commands.git (fetch)
   origin  https://github.com/jaybjackie/git-commands.git (push)
   ```

2. View details about a remote repo named `origin`, including all the remote branches and local tracking branches for `origin`:
   ```
   git remote show origin
   ```


3. (Pushing a new branch) You commit some files to the `dev-foo` branch and try to "push" them to Github, but it fails as shown here:

   ```
   cmd>  git checkout dev-foo
   cmd>  git push
   fatal:  The current branch dev-foo has no upstream branch. 
   ```
   Explain this error.

   > This error occurs when we have push current branch on remote repo but there is zero branch on remote repo(tends occur when newly create Git repo).

4. The command to push `dev-foo` to `origin` as a **new remote branch** on `origin` is:

   ```
      git push --set-upstream origin dev-foo
   ```


5. (Create a local tracking branch for a remote branch) The remote repository (`origin`) has a branch named `e2e-test` that you don't have in your local repository.   
   The command to create a new local branch as a copy of the remote `e2e-test` branch that **tracks** the remote branch is:
   ```
   git branch --track e2e-test origin/e2e-test 
   ```

6. Consider this situation:
   - you have a local repository with a remote repo on Github
   - Your local repo is up-to-date with the remote repo on Github!
   - You edit `README.md` on Github using Github's web interface and save the changes.
   - On your local machine, you edit README.md, commit the changes locally
   
   What happens when you `push` your changes?    
   Explain why and how to fix it.

> push not success because their is changed from remote repo, local repo and remote one is different and conflict will occur.
>To Fix: 
   ```
   # downloads changes from origin
   git fetch
   # automatically merge branches, --no-commit gives you a chance to review the results
   git merge --no-commit
   # resolve the conflict
   # git status to see there is conflict
   git status
   # done solving, then add, commit and push.
   git add README.md
   git commit -m "<your-massage-here>"
   git push
   ```

> In case there are too many conflict, you are done with it.
```
git merge --abort
```
> to undo the merge and try something else.


7. The command to change the URL of the remote "origin" to a new URL, such as `https://hostname/newuser/new-repo-name`, is:
   ```
   git remote set-url origin https://hostname/newuser/new-repo-name
   ```
   This situation occurs when:
   - you change the name of a repo on Github
   - you transfer ownership of a Github repo to someone else
   - you move from Github to another hosting site, like Bitbucket
   - you want to switch from the https to the ssh protocol (the remote URL is different even though location is the same)    


8. To create a *second* remote repository for your local repo, the command to add a remote named "bitbucket" with the URL "https://bitbucket.org/your-username/git-commands" is:
   ```
   git remote add bitbucket https://bitbucket.org/your-username/git-commands
   ```
   - Note: you must **create** an empty repo on Bitbucket. This command just adds it as a remote, it won't create the remote repo.


9. After adding the remote named `bitbucket`, the command to push your master branch to `bitbucket` is:
   ```
   git push origin bitbucket
   ```

