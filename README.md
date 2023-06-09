# GitAndGitHub

## Git Commands

- See the currently available git branches 

``` 
    git branch 
```

- Create a new branch 

``` 
    git checkout -b <branch_name> 
```

- Check the differences and compare two git branches

``` 
    git diff <branch_name>  
```

- Check the git status

``` 
    git status 
```

- Start tracking the files

``` 
    git add <file_name>  (For tracking a single file)
    git add .            (For tracking all the files)
```

- Staging the tracked files

``` 
    git commit -m <commit_message_tile> -m <commit_message_description> 
```

- Unstage the tracked files. Used to UNDO a git add

```
    git reset   
```

- Reset and go to a particular commit back in history

```
    git reset <commit_hash>
```

- Unstage and untrack the tracked files. Used to UNDO a git commit

```
    git reset HEAD~1 
```

- Pushing the current state of the branch into the remote GitHub repository

``` 
    git push origin <branch_name>   
```

- See the git commit history and logs

``` 
    git log 
```