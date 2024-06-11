# GitAndGitHub

## Concepts and Terminologies

- .git DIRETORY

```
    The .git directory (which is normally a hidden directory) stores all the information for the
    Version Control System
```

- HEAD

```
    Currently active or checked out branch
```

- HOOKS

```
    These are files present in the .git/hooks directory that are used to fire off custom
    scripts when certain important actions occur. There are two groups of these hooks:
    client-side and server-side. Client-side hooks are triggered by operations such as
    committing and merging, while server-side hooks run on network operations such
    as receiving pushed commits
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

- PULL REQUESTS (PRs)

```
    A pull request is a way to request to pull your code and merge it with the intended branch
    It serves as a way to showcase the code and for code reviewing and discussing before
    it is actually merged into the intended branch
```

- FORK

```
    A complete copy of the original GitHub repository where changes and pull requests can
    be made
```

- INIT

```
    Used to create an empty git repository or reinitialize an existing git repository
```

- STAGE

```
    Staging means to bring the untracked and modified files to the staging area before
    a snapshot is being taken through the commit command
```

- STASH

```
    Stashing means to temporarily shift and keep the staged files aside from the staged
    area without actually committing the staged files. These stashed files and be brought
    back as and when required to the staging area
```

- COMMIT

```
    Clicking a snapshot of the currently staged files
```

- BISECT

```
    Uses Binary Search to find the exact commit that introduced a bug. The commits can be
    seen as a monotone space : [1,1,1,1,1,....,1,1,0,0,0,0,....,0] where 1 represents good
    commit and 0 represents bad commit. Hence we can find the first bad commit  and track
    from which commit our code exploded
```

- CHERRY-PICK

```
    Cherry-picks a particular commit (usually from some other branch, by its hash value)
    and then adds it on top of my current branch and creates a new commit. This is used
    when I do not want all the commits or changes of that feature branch and wish to have
    some specific commits of that feature branch on top of my local branch
```

- SQUASH

```
    Merging multiple commits into a single commit so as to remove dirty commits and
    keep the workflow clean
```

- REBASE

```
    An alternative to merge, where all the commits of the feature branch is moved and
    shifted on top of the master/main branch. In this way, the commit history of the
    feature branch can be added on top of the master/main branch. However, in case of
    merge, the intermediate commits in the feature branch are lost and only a single
    new commit is added on top of the master/main branch
```

- PUSH

```
    Make the changes that were just committed visible and available on top of the local
    git branch or the remote GitHub branch
```

- FETCH

```
    Fetch the recently made changes in the remote origin branch or the remote upstream
    branch to our local git branch. Fetch creates a separate branch and does not merge
    with our current branch. Hence we can check the diff and modifications without
    merging into out branch
```

- PULL

```
    Pull the recently made changes in the remote origin branch or the remote upstream
    branch to our local git branch. Pull fetches and merges the changes with our current
    branch. Basically, pull = fetch + merge
```

- SUBMODULE

```
    A submodule is a git repository within another git repository. Basically it's a
    nested git repository. This is mostly used when we want to use some third-party
    code or libraries into our own code. We create a separate submodule for the
    third-party repo with the required libraries. This way we can keep track of
    main git repo and the submodule repo simultaneously
```

## Analogy with my Crush

> _As I waltzed into the mesmerizing venue of my crush's birthday extravaganza, my heart skipped a beat. It was a sight to behold, just like a perfectly organized repository with files and folders neatly arranged. Little did I know that my journey as a photographer would soon become entangled with the art of git, leading to a hilarious and insightful analogy._
>
> _In this grand affair, I, the humble photographer, played the role of git itself. Like git, I had the power to capture moments and preserve them for eternity. But first, I needed the perfect camera to match the occasion. My trusty gear was divided into three branches—each with its unique flair. The DSLR branch would capture crisp and high-quality snapshots, the SLR branch was dedicated to timeless classics, and the video camera branch added a touch of motion to the memories._
>
> _As the night unfolded, it was time to bring the guests and invitees onto the stage. They were like the files and folders, waiting to be showcased. With the finesse of a git command, I would add and stage each guest onto the podium. Clicking my camera shutter was akin to capturing those delightful moments in a snapshot._
>
> _Now, here's where the fun began. I had a choice: either commit the snapshot directly and save a local version in my camera—just like committing changes in git—or I could request the guests to hold on and retreat to the backstage. Why, you ask? Well, I had some tricks up my sleeve. I wanted to experiment with lighting arrangements, enhance features, and surprise everyone with dazzling effects. This act of whisking the guests away to the backstage was my personal way of stashing._
>
> _With the guests waiting patiently behind the scenes, I would unleash my creative genius. It was as if I were making changes to my code, tweaking and refining the atmosphere. And when the time was right, I would bring the guests back onto the stage, one by one, unveiling the wonders of my imagination._
>
> _Just like an artist unstash changes, I would call them back, and their presence would grace the spotlight once again. The crowd would gasp in awe as I captured their radiant smiles and infectious laughter. Unstashing changes was my way of showing the world the hidden gems I had crafted, while ensuring that the main stage remained a spectacle._
>
> _Once I was satisfied with my snapshots, it was time to immortalize them. Just as I had local copies in my camera from committing, I could now publish those snapshots in a grand photo album. And where else would I host this album of wonders? None other than the remote GitHub repository, a digital realm where my photographs could shine for all to see._
>
> _So, just like I immortalized my crush's special day through my lens, Git mirrored my journey as a photographer, preserving the history of my art, tracking improvements, and GitHub by sharing them with the world. It was a perfect blend of artistry, technology, and a little bit of wit—much like the way my crush lit up the room with her charm and effortlessly stole the show with her magnetic charm._
>
> _Therefore, my dear friends, let us raise a toast to the birthday bash that merged the realms of love and git, reminding us that in the grand symphony of life, even the quirkiest analogies can reveal profound truths._

## Git Commands

### Git Status and Monitoring

- Check the .git directory

```console
    ls -a
```

- Check the git status

```console
    git status
```

- See the currently available git branches

```console
    git branch      (Shows all the currently available git branches)
    git branch -v   (Shows the currently available git branches along with their details)
```

- See the git commit history and logs

```console
    git log
    git log --oneline
    git log --graph
    git log --graph --oneline --decorate
```

- See git object history including blobs, trees, commits in a textual format

```console
   git show 
```

- Add Remote ORIGIN

```console
    git remote add origin <remote_origin_url>
```

- Add Remote UPSTREAM

```console
    git remote add upstream <remote_upstream_url>
```

- Set Remote ORIGIN (Modify existing URL)

```console
    git remote set-url origin <remote_origin_url>
```

- Set Remote UPSTREAM (Modify existing URL)

```console
    git remote set-url upstream <remote_upstream_url>
```

- See the remote URLs that are set

```console
    git remote -v
```

### Git Cloning, Branching, Tracking, Merging, Pushing, Pulling and Deleting

- Cloning a remote GitHub Repository

```console
    git clone <remote_GitHub_Repository_URL>
    git clone --recurse-submodules <remote_GitHub_Repository_URL>
```

- Initializing the git submodules after cloning from a remote GitHub Repository

```console
    git submodule update --init --recursive
```

- Create a new git branch

```console
    git checkout -b <branch_name>
    git branch <branch_name>
```

- Rename the current git branch

```console
    git branch -m <new_branch_name>
```

- Switch to just the previous git branch

```console
    git switch -
```

- Switch to another git branch

```console
    git switch <branch_name>
```

- Check the differences and compare a git branch to the current git branch

```console
    git diff <branch_name>
```

- Delete an available local git branch

```console
    git branch -d <branch_name>
```

- Delete an available remote git branch

```console
    git branch --delete --remotes <origin/branch_name>
    git branch --delete --remotes <upstream/branch_name>
```

- Delete an available remote GitHub branch

```console
    git push origin --delete <github_branch_name>
```

- Fetch the latest remote changes

```console
    git fetch origin
    git fetch upstream
    git fetch upstream --prune
```

- Pull the latest changes from a remote branch

```console
    git pull origin     <branch_name>   (Pull from user's personal forked remote branch)
    git pull upstream   <branch_name>   (Pull from original project's remote branch)
```

- Cherrypick a particular commit from some other feature branch and add on top of the current branch

```console
    git cherry-pick <commit_hash>
```

- Merge a particular branch into the HEAD or current branch

```console
    git merge <branch_name>
```

- Rebase a particular branch with the main/master (Sync with main/master - checks the possibility of merge conflicts)

```console
    git switch <branch_name_to_be_rebased>
    git rebase main
    git rebase master
```

- Move and shift the rebased branch commits on top of the master/main branch and then blow off the rebased branch

```console
    git switch main
    git switch master
    git rebase <branch_name_that_was_rebased>
```

- Stage the unstaged files

```console
    git add <file_name>  (For tracking a single file)
    git add .            (For tracking all the files)
```

- Stash the staged files

```console
    git stash
    git stash push -m <stash_message>
```

- See the stash stack

```console
    git stash list
```

- Apply a particular stash from the stash stack

```console
    git stash apply <stash_id>
```

- Create a new branch with a particular stash on top of the current HEAD

```console
    git stash branch <branch_name> <stash_id>
```

- Pop the stashed files (Apply the stash and delete it from the stack - Apply + Drop)

```console
    git stash pop <stash_id>
```

- Drop or Delete a particular stash from the stash stack

```console
    git stash drop <stash_id>
```

- Clear or delete all the stashed files from stash stack

```console
    git stash clear
```

- Commit or click a snapshot of the staged files

```console
    git commit -m <commit_message_title> -m <commit_message_description>
    git commit
```

- Push the current state of the branch into the remote GitHub repository

```console
    git push origin <branch_name>
    git push origin <branch_name> -f    (Force Push)
```

- Delete a particular file from the git index permanently

```console
    git rm <file_name>
```

- Delete/Untrack a particular file from the git index but keep it in the present working directory

```console
    git rm --cached <file_name>
```

- Rename a particular file

```console
    git mv <old_file_name> <new_file_name>
```

- Move a particular file

```console
    git mv <old_file_name> <new_file_name_location>
```

### Git Undoing and Going Back In Time

- Unstage the tracked files. Used to UNDO a git add

```console
    git reset
```

- Reset and go to a particular commit back in history

```console
    git reset --hard <commit_hash>
```

- Unstage and untrack the tracked files. Used to UNDO a git commit

```console
    git reset HEAD~1
```

- Debug the exact commit which introduced a bug

```console
    git bisect start
    git bisect good <good_commit_hash>
    git bisect bad <bad_commit_hash>
    git bisect good/bad
```

- Restoring a deleted file

```console
    git restore <file_name>
```

- Restoring a file to keep some of the modified portions of the file and discard some of the modified portions

```console
    git restore -p <file_name>
```

## Use Cases

### Q. How to gitignore contents of a folder but track the folder itself and push it to GitHub?

To push empty folders to GitHub, we directly cannot commit empty folders in git. However, if we want an empty folder to show up, we need to put something in it, even just an empty file.

By convention, we add an empty file called .gitkeep to the folder that we want to keep, then in the
.gitignore file, we add:

```console
# ignore everything inside the folder
emptyFolderWeWishToShowUp/*

# exception to the rule, to keep the folder
!emptyFolderWeWishToShowUp/.gitkeep
```
