Git has 3 environments 

Working files ---> Staging ---> Commit 

GIT STATUS
Check the status of the files
    ```git status

TRACK AND UNTRACK FILES
Track the files
    ```git add <file-name>

Untarack it 
    ```git rm --cached <file-name>

TRACK ALL FILES
Track all files
    ```git add .

COMMIT 
Creating a snapshot or writing an entry in history book
    ```git commit -m "your message"

MODIFY A FILE
View Differences
    ```git diff 
    later press q to exit

If you are not ready with the changes go back to working file mode
    ```git restore --staged <file-name>

BYPASS THE STAGING PHASE I.E. FROM WORKING DIRECTLY TO COMMIT (Not recommended)
    ```git commit -a -m "your message"

DELETE A FILE
Delete file command 
    ``` git rm "<file-name>"
 But if you change your mind --- lolol like me 
    ```git restore "<file-name>"

RENAME A File
    ```git mv  "<old-file-name>" "<new-file-name>"

REVIEW COMMITS DONE SO FAR
    ```git log (commits with detailed desc)
    ```git log --oneline (this is for one line details)


    AMMEND A COMMIT (Rather than going the long way -- correct the previous commit)
        ```git commit -m "your correct message" --amend

    DIG INTO THE SPECIFICS -- CHECK WHAT COMMITS WERE DONE
        ```git log -p

    MODIFY THE ORDER OF COMMITS 
        ```git rebase -i --root
        goes to edit 
        press :x enter

BRANCHES 
Basically a copy of your main branch - has all entries 
used usually during bug fix 

    CREATE A NEW BRANCH
        ```git branch branchName

    CHECK NUMBER OF BRANCHES YOU HAVE 
        ```git branch
    
    SWITCH TO ANOTHER BRANCH
        ```git switch branch-name

    MERGE YOUR CHANGES FROM YOUR BRANCH TO MAIN BRANCH
        ```git merge -m "your merge message" branch-name

