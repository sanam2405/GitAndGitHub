# GitAndGitHub

## Git Commands

### Git Status and Monitoring

- Check the git status

``` 
    git status 
```

- See the currently available git branches 

``` 
    git branch 
```

- See the git commit history and logs

``` 
    git log 
```


### Git Tracking, Branching, Pushing and Pulling


- Create a new branch 

``` 
    git checkout -b <branch_name> 
```

- Check the differences and compare two git branches

``` 
    git diff <branch_name>  
```

- Start tracking the files

``` 
    git add <file_name>  (For tracking a single file)
    git add .            (For tracking all the files)
```

- Staging the tracked files

``` 
    git commit -m <commit_message_title> -m <commit_message_description> 
```

- Pushing the current state of the branch into the remote GitHub repository

``` 
    git push origin <branch_name>   
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