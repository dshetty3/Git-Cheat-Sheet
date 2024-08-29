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
