# Add a new repositority (I always forget this and end up messing with my files lololololol :D)

Initially create a repo in your github account
1. git init
2. git add README.md
3. git commit -m "first commit"
4. git branch -M main
5. git remote add origin https://github.com/dshetty3/test.git - Assuming u have it ready in your git account
6. git push -u origin main


# GitCommands 
Ofcourse I need this since I need a ton of practice for git. Feel free to use it.


Git Hub Cheat Sheet

1. Basic commands:

1.1 Installing git on terminal 
	Step 1: Open terminal and type “sudo opt install git” 
	Step 2: type “yes” when prompted 
	Step 3: You have successfully installed git

# Create a file in your desired location or the project u wish to work on, travel to that path in putty and then follow the below commands step by step


1.2 Most used commands
	1.2.1 git cloned URL - initial work - once cloned add the files up desire to push in the newlt cloned file 
	1.2.2 git status - any changes in files will be shown here
	1.2.3 git add filename - single file u wish to push
	1.2.4 git add . -a - all files present on the repository
	1.2.5 git commit -m "Initial Commit"
	1.2.6 git push - local to git
	1.2.7 git pull - merge code from git to local
	1.2.8 git all commands 
	

1.3 Using SSH to access a repository
	1.3.1 ssh-keygen -t rsa -b 4096 -C “email.com”
	1.3.2 -enter
	1.3.3 -passphrase

	1.3.4 new terminal 	
	1.3.5 cd .ssh
	1.3.6 gedit id_rsa.pub
	1.3.7 copy the key
	
	1.3.8 go the the website
	1.3.9 settings ssh and gpg keys – add new ssh key
	1.3.10 add title 
	1.3.11 paste the key from step 1.3.7

	1.3.12 new terminal
	1.3.13 eval “$(ssh-agent -s)”
	1.3.14 ssh-add
	1.3.15 enter passphrase

	1.3.16 git clone ssh url
 	1.3.17 cd test i.e cd reponame
	1.3.18 git filename filetype
	1.3.19 git add filename filetype
	1.3.20 git commit -m “msg”
	1.3.21 git push 
	1.3.22 git status
	


Git and GitHub Lessons

Git is a version control system (VCS). A VCS help a software team manage changes to the source code over time. 

1. VCS software include tools for saving the state of a project
2. Viewing the history of changes
3. and reverting changes.

Developing software without VCS is risky similar to not having backups.

VCS can also Enhance and Speed up development.
Depending on the version control software used many developers can work on the same code at the same time.
VCS can even have tools to prevent conflicts when one developers changes are incompatible with changes made at the same time by another developer. 

Version control software examples: Git, Concurrent Versions System (CVS), GitLab, BitBucket, SourceForge. 


1. Why use git?
Git is the most popular version control system it is mature, actively maintained, open-source and compatible with many operating systems and IDE’s. Git is different from other operating system in the way of recording changes. Othe systems record changes by adding it to the database. Git records changes as a stream of shapshots.

Another advantage of Git – it is distributed rather than having only one single place for the full version history of a project, every developer’s working copy of the code is also a repository that can contain the full history of all changes. 

2. History of git
Git was created by Linus Torvalds in 2005 for development of the linux kernel, with other kernel developers contributing.

Git – Global information tracker. 

How to use Git.
The most effective way to run git is through a command line prompt. 

Step1 : Create a directory by using – mkdir my_git_folder
Step2 : cd my_git_folder
Step3 : to turn the empty folder to git repository – git init

Difference between Git and GitHub. 
Git is a Version Control System for managing your source code history and GitHub is a hosting for your Git Repositories.


Tracking Files.

In general, files in a repository can have the following statuses: 
1. Not Tracked
2. Staged
3. Committed

To find the actual status of a file in your repository use the git status command.
Step1: create a file readme.txt

Step2: git status

Step3: the file is untracked 

Step4: It means that the file is untracked by git for changes. We should explicitly say which file to track for changes.

Step5: for that use git add “filename” command to tell git that track the file. This step is called staging.

Note: If you dont want git track some files such as passwords that you dont want other to see in your repository then use .gitignore file 

Use touch .gitignore in Linux to simply create a new file.

After the staging area we need to add the file to our repository for that use git commit.

Git Commit.

The git commit command saves the state of your project by adding a snapshots of stages files to the repository.

Use the command git commit -m “msg” command to add the file to your repository.

The -m flag with a msg describing what we’ve changed.
 
To commit modifications for every tracked file in the repository, use git commit -a -m “commit all”
To see the history of your commits use the git log command.

Cloning and Pushing.

After commiting the changes, the next step is to push the local repository to the a remote location on Git server.
We have the following option:
1. clone or download the repository and start making changes
2. to initialize a local repositiory and then connect it with the remote one

clone command:
git clone https://www.github.com/user/project_name.git

if you have already initialized a local repository, you can connect it to the remote one using the following command:
git remote add origin https://www.github.com/user/project_name.git
 
Pusing Remotely:
Making our changes locally and commiting to the remote repository
the push command tells git where to put our commits
git push -u origin master
 
-u the -u tells git to remember the parameters, so that next time git push is run we can simply write git push instead of the entire command.



Pulling.
Command: 
git pull origin master 

We can check whats different from our last commit by using the git diff HEAD command 
We want the diff of our most recent commit, which we can refer to using the HEAD pointer.

Reset & Checkout.

 You can us diff to look at changes within files that have already been staged. Running git diff –staged  will show the changes you just staged.

A stage can also be rest using the reset command :
git reset ‘filename’

This removes the file from the staged status, meaning that all the changes will still remail in the file.

To reset the file to the lates committed version the checkout command is used
git checkout -- ‘filename’ 

Branching.

Command :
git branch my_new_branch

To switch to the branch:
git checkout my_new_branch

There is a shortcut to create and switch to a new branch:
git checkout -b my_new_branch

To see the list of branches use the command:
git branch

Amend.

The git commit –amend command is a convenient way to modify the most recent commit.
It lets you combine the staged changes with the previous commit instead of creating an entirely new commit.

It can also be used to simply edit the previous commit message:
git commit –amend -m “update commit message” 

the -m option allow you to pass in a new message for the latest commit.

Stash.

The git stash command temporarily caches any changes you’ve made to the working copy so you can switch to something else, and then come back later and recover them.

The git stash command takes your uncommitted changes both staged and unstaged, and saves them for later use 
git stash

There are 2 way to re-load the stashed changes:
git stash pop

the pop will remove stashed changes from the stashed state

git stash apply

the apply command will apply the same stashed changes to multiple branch

Git stash will not include untracked files by default. To do so, we should add the -u option (or –include-untracked)

Merging Branches.

Create file in the main branch:
The following command will create 5 files named file1 .. file5 
touch file{1 ..5}.txt
git add .
git commit -m "add file 1 to 5"

Create a new branch: 
git checkout -b test

Remove files from main branch and add some files to the test branch
touch file{6 ..10}.txt
git rm file3.txt
git rm file4.txt 
git add .
git commit -m "added files and removed 3&4"
Now merge the two branches:
git checkout master
git merge test

To remove a branch you dont need anymore use:
git branch -d test

Merge Conflicts.

If a file is changed in both the master and test branch and there are different version of the same file in both the branches then merge conflict occurs.

The merge conflict is indicated with the <<<<<<<, =======, >>>>>>> conflict markers. 

You will have to fix this conflict manually and commit the changes.
Remove the conflict markers and make the changes you want in the final merge. Save and exit. Finally, commit your changes.