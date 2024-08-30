# My GIT and GitHub Learning

## GIT (Local repo)
Git has 3 environments 

Working files ---> Staging ---> Commit

## CONFIGURE NAME AND ADDRESS
- **Configure name:** 
```bash
   git config --global user.name "your name"
```

- **Configure email:** 
```bash
   git config --global user.email your email
```
- **Initialize default branch name:** 
```bash
   git config --global init.default branch main
```

## GIT STATUS
- **Check the status of the files:** 

```bash
    git status
```
## TRACK AND UNTRACK FILES
- **Track the files:** 
```bash
    git add <file-name>
```
- **UnTrack:** 
 ```bash 
     git rm --cached <file-name>
```
- **Track all Files:** 
 ```bash 
     git add .
 ```

## COMMIT
- **Creating a snapshot or writing an entry in history book:** 
```bash
    git commit -m "your message"
```
## MODIFY A FILE
- **View Differences:** 
```bash
    git diff
```
   later press q to exit

1. If you are not ready with the changes go back to working file mode:
```bash
    git restore --staged <file-name>
```
## BYPASS THE STAGING PHASE
```bash
    git commit -a -m "your message"
```
## DELETE A FILE
- **Delete file command:**
```bash
    git rm <file-name>
```
- **But if you change your mind --- lolol like me:**
```bash
    git restore <file-name>
```
## RENAME A FILE
```bash
    git mv  "<old-file-name>" "<new-file-name>"
```
## REVIEW COMMITS DONE SO FAR
```bash
    git log (commits with detailed desc)
    git log --oneline (this is for one line details)
```
## AMMEND A COMMIT (Rather than going the long way -- correct the previous commit)
```bash
   git commit -m "your correct message" --amend
```
## DIG INTO THE SPECIFICS -- CHECK WHAT COMMITS WERE DONE
```bash
   git log -p
```
 ## MODIFY THE ORDER OF COMMITS 
```bash
   git rebase -i --root
```
goes to editor 
press :x enter

## BRANCHES
Basically a copy of your main branch - has all entries used usually during bug fix 

```bash
# CREATE A NEW BRANCH
git branch branchName

# CHECK NUMBER OF BRANCHES YOU HAVE 
git branch

# SWITCH TO ANOTHER BRANCH
git switch branch-name

# MERGE YOUR CHANGES FROM YOUR BRANCH TO MAIN BRANCH
git merge -m "your merge message" branch-name

# DELETE THE BRANCH
git branch -d FixTemp

#SWITCH TO NEW BRANCH WHILE CREATING IT
git switch -c branchName
```

## MERGE CONFLICTS
```bash

#SWITCH TO NEW BRANCH WHILE CREATING IT
git switch -c branchName

#COMMIT FOR BRANCH CHANGES
git commit -a -m "Update Branch changes"

#SWITCH TO MAIN
git switch main

#COMMIT FOR MAIN CHANGES
git commit -a -m "Update Main changes"

#MERGE CHANGES FROM BRANCH TO MAIN
git merge branchName --- merge fail because of conflicts edit it in editor 
```


## GITHUB (Cloud repo)


