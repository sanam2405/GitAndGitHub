# GitAndGitHub

## Git Commands

- See the currently available git branches 

``` git branch ```

- Create a new branch 

``` git checkout -b <branch_name> ```

- Check the differences and compare two git branches

``` git diff <branch_name>  ```

- Check the git status

``` git status ```

- Start tracking the files

``` 
    git add <file_name>  (For tracking a single file)
    git add .            (For tracking all the files)
    
```

- Staging the tracked files

``` git commit -m <commit_message_tile> -m <commit_message_description> ```

- Untrack and unstage the tracked files

``` git restore HEAD~1 ```

- Pushing the current state into the remote GitHub repository

``` git push origin <branch_name>   ```