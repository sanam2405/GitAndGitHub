# GitAndGitHub

## Concepts and Terminologies

- HEAD

``` 
    Currently active or checked out branch
```

- ORIGIN

```
    Name given to the URL to the user's personal forked remote GitHub repository
```

- UPSTREAM

```
    Name given to the URL of the original project remote GitHub repository
```

- LOCAL BRANCHES

```
    The branches that are present locally in our machine after the git directory is setup
```

- REMOTE BRANCHES

```
    The branches that are present remotely in GitHub
```

- Pull Requests (PRs)

```
    A pull request is a way to request to pull your code and merge it with the intended branch
    It serves as a way to showcase the code and for code reviewing and discussing before
    it is actually merged into the intended branch
```

- FORK

```
    A complete copy of the original GitHub repository where changes and pull requests can be made
```

- .git DIRETORY

```
    The .git directory (which is normally a hidden directoy) stores all the information for the Version Control System
```

## Git Commands

### Git Status and Monitoring

- Check the .git directory

``` 
    ls -a 
```

- Check the git status

``` 
    git status 
```

- See the currently available git branches 

``` 
    git branch      (Shows all the currently available git branches)
    git branch -v   (Shows the currently available git branches along with their details)
```

- See the git commit history and logs

``` 
    git log 
```

- See the remote URLs that are set 

``` 
    git remote -v
```


### Git Branching, Tracking, Pushing and Pulling


- Create a new git branch 

``` 
    git checkout -b <branch_name> 
    git branch <branch_name>
```

- Rename the current git branch

```
    git branch -m <new_branch_name>
```

- Switch to another git branch

```
    git switch <branch_name>
```

- Check the differences and compare a git branch to the current git branch

``` 
    git diff <branch_name>  
```

- Delete an available git branch

```
    git branch -d <branch_name>
```

- Delete an available remote GitHub branch

```
    git push origin --delete <github_branch_name>
```

- Fetch the latest remote changes

```
    git fetch origin
```

- Pull the latest changes from a remote branch

```
    git pull origin     <branch_name>   (Pull from user's personal forked remote branch)
    git pull upstream   <branch_name>   (Pull from original project's remote branch)
```

- Stage the unstaged files

``` 
    git add <file_name>  (For tracking a single file)
    git add .            (For tracking all the files)
```

- Stash the staged files

```
    git stash
```

- Pop the stashed files

```
    git stash pop
```

- Clear or delete the stashed files

``` 
    git stash clear
```

- Commit or click a snapshot of the staged files

``` 
    git commit -m <commit_message_title> -m <commit_message_description> 
```

- Push the current state of the branch into the remote GitHub repository

``` 
    git push origin <branch_name>   
    git push origin <branch_name> -f    (Force Push)
```

### Git Undoing and Going Back In Time

- Unstage the tracked files. Used to UNDO a git add

```
    git reset   
```

- Reset and go to a particular commit back in history

```
    git reset --hard <commit_hash>
```

- Unstage and untrack the tracked files. Used to UNDO a git commit

```
    git reset HEAD~1 
```

- Restoring a deleted file

```
    git restore <file_name>
```

- Restoring a file to keep some of the modified portions of the file and discard some of the modified portions

```
    git restore -p <file_name>
```

