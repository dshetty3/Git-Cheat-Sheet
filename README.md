Git has 3 environments 

Working files ---> Staging ---> Commit 

1. GIT STATUS
    Check the status of the files
        ```git status

2. TRACK AND UNTRACK FILES
    Track the files
        ```git add (file-name)

    Untrack it 
        ```git rm --cached (file-name)

3. TRACK ALL FILES
    Track all files
        ```git add .

4. COMMIT 
    Creating a snapshot or writing an entry in history book
        ```git commit -m "your message"

5. MODIFY A FILE
    View Differences
        ```git diff 
        later press q to exit

If you are not ready with the changes go back to working file mode
    ```git restore --staged (file-name)

6. BYPASS THE STAGING PHASE I.E. FROM WORKING DIRECTLY TO COMMIT (Not recommended)
    ```git commit -a -m "your message"

7. DELETE A FILE
    Delete file command 
        ``` git rm "(file-name)"
    But if you change your mind --- lolol like me 
        ```git restore "(file-name)"

8. RENAME A File
    ```git mv  "(file-name)" "(file-name)"

9. REVIEW COMMITS DONE SO FAR
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

10. BRANCHES 
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

    DELETE THE BRANCH
        ```git branch -d FixTemp

    SWITCH TO NEW BRANCH WHILE CREATING IT
        ```git switch -c branchName

11. MERGE CONFLICTS


