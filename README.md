# Learning-Git
Commands and Thier uses for working with git

THIS IS AVALIABLE IN NOTES.TXT REST FILES ARE JUST CREATED TO DEMONSTRATE 
INITIALISE NAME AND EMAIL
*****************************************************************
Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO
$ git config --global user.name Naman

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO
$ git config --global user.email a.naman@iitg.ac.in

TO SEE NAME AND EMAIL
*****************************************************************
Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO
$ git config --global user.email
a.naman@iitg.ac.in

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO
$ git config --global user.name
Naman



*****************************************************************
*****************************************************************
CREATE EMPTY GIT REPOSITORY 
*****************************************************************
Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO
$ git init
Initialized empty Git repository in C:/Users/Dell/Desktop/GIT IN ONE VIDEO/.git/

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ ls -lart   (SHOWS ALL HIDDEN FOLDERS)
total 12
drwxr-xr-x 1 Dell 197121 0 Feb 18 00:58 ../
drwxr-xr-x 1 Dell 197121 0 Feb 18 01:02 ./
drwxr-xr-x 1 Dell 197121 0 Feb 18 01:02 .git/

ALL THE DATA IS IN .git folder created here
*****************************************************************
*****************************************************************
UNTRACKED : WE ARE NOT TRACKING USING GIT 
ONCE WE ADD TO GIT AND RECORD CHANGES TO GIT FILE

UNTRACKED------------------------------>---------STAGED
                                   ADD THE FILE
STAGED AREA : WHERE WE WILL COMMIT
(LIKE PLAYGROUND)
COMMIT : SNAPSHOT 

STAGING AREA WE PASS THOSE WE WANT TO WORK WITH 
WE STAGE THOSE WHO WANT TO 

STAGING AREA ------------------->-----------------UNMODIFIED
                                           COMMIT
THIS FILE HAS SENT TO SNAPSHOT 
THIS FILE WE CAN EDIT / REMOVE / OR LEAVE


UNMOFIFIED------------>--------------MODIFIED
                                   EDIT THE FILE

MODIFIED----------->---------------STAGED
AGAIN PASS TO STAGE
THEN AGAIN U COMMIT 


*****************************************************************
*****************************************************************

IT IS SAYING UNTRACKED FILE

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        NOTES.txt
        index.html

nothing added to commit but untracked files present (use "git add" to track)

*****************************************************************
git status TELLS which files are not added and which are added

U can add by 
git add FileName(autocomplete use tab)

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git add NOTES.txt

*****************************************************************
One initial Commit is required to track Project 

WE WRITE GIT COMMIT 

IT WILL OPEN VIM EDITOR

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch master
#
# Initial commit
#
# Changes to be committed:
#       new file:   NOTES.txt
#       new file:   index.html
#
# Changes not staged for commit:
#       modified:   NOTES.txt
#
~
~
~


HOW TO START HERE :
PRESS I TO START TYPING
AND WRITE Initial commit
Press Escape and then :wq to exit

THIS INITIAL COMMIT IS THE MESSAGE WE HAVE GIVEN TO FILE CHANGE 

NOW IT WILL DISPLAY THIS 

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git commit
[master (root-commit) 53792a1] Initial Commit
 2 files changed, 102 insertions(+)
 create mode 100644 NOTES.txt
 create mode 100644 index.html

*****************************************************************
Now use git status it will display 
$ git status 
On branch master 
nothing to commit, working tree clean

IF WE PUT CHANGES TO FILE
*****************************************************************
touch about.html
touch contact.html

TOUCH COMMAND IS USED TO CREATE NEW FILE

*****************************************************************
adding many FILES TOGETHER 

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git add -A
*****************************************************************
NOW COMMIT 
IF U WANT TO DIRECTLY ADD MESSAGE THEN USE 
WITHOUT GOING TO VIM EDITOR

USE :
git commit -m "Added More Htmls"
*****************************************************************
clear is used to clear terminal
$ clear
*****************************************************************
IF SOMEONE HAS REMOVED OR CHANGED OUR FILE AND 
WE WANT TO RETRIVE BACK WE CAN USE CHECKOUT COMMAND

git checkout Filename
git checkout -f (IF U WANT ALL FILES TO COME BACK AGAIN)

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git checkout NOTES.txt
Updated 1 path from the index
*****************************************************************
Commit u mean U CAN RECOVER ANYTIME SO COMMIT ONCE U HAVE DONE 
AND DON'T FORGET 
*****************************************************************
IF U WANT TO CHECK WHEN WAS LAST EDITED 
THEN USE 
git log


$ git log
commit 0602c699ffe13793d2ba54cbbe6800da4b59be59 (HEAD -> master)
Author: Naman <a.naman@iitg.ac.in>
Date:   Fri Feb 18 11:36:16 2022 +0530

    Modified Notes

commit 35c045411a37e22529554679e586a4deb0ce4d2d
Author: Naman <a.naman@iitg.ac.in>
Date:   Fri Feb 18 11:31:18 2022 +0530

    For Recovering

commit 8ea887beaaea59a88cde4a7254f10135ef0fd51b
Author: Naman <a.naman@iitg.ac.in>
Date:   Fri Feb 18 11:28:57 2022 +0530

    Added More Htmls

commit 53792a1a5d4cffd15ff985f7ce5253cc3615fc66
Author: Naman <a.naman@iitg.ac.in>
Date:   Fri Feb 18 11:17:04 2022 +0530

    Initial Commit

IF WE WANT TO FILTER GIT LOG 
SEE LAST 5 THEN 
git log -p -5

NOW IT WILL ALSO TELL ALL THE CHANGES U MADE 
Now u use q to quit 
****************************************************************
git diff will show what u changed without pushing into staging area
If no change then this command will not show anything 
****************************************************************
If U want to compare staging area with last commit then use 
git diff --stage
****************************************************************
****************************************************************
****************************************************************
THERE IS A DIRECT METHOD TO COMMIT ALSO BUT TRY TO AVOID 

git commit -a -m

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git commit -a -m "Skip Staging Area and Commit"
[master 7fed1de] Skip Staging Area and Commit
 1 file changed, 7 insertions(+)

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git log -1
commit 7fed1de18dac9c7ed26dc3683b04944138083cb5 (HEAD -> master)
Author: Naman <a.naman@iitg.ac.in>
Date:   Fri Feb 18 11:49:33 2022 +0530

    Skip Staging Area and Commit
****************************************************************
U can use git Bash as terminal also

How to remove a file 

$ git rm --cached waste
rm 'waste'
IT WILL MOVE THE FILES TO UNTRACKED AREA 

$ git rm waste
rm 'waste'
IT WILL DELETE THE FILE
****************************************************************
****************************************************************
git status -s

TO TRACK MANY FILES ( SHORTHAND)

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git status -s
 M NOTES.txt

it tells the Files modified 
****************************************************************
Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git status -s
 M NOTES.txt
 M about.html
 M contact.html

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git add contact.html

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git status -s
   M NOTES.txt
   M about.html
M    contact.html

THE FIRST M DENOTES THAT IT HAS BEEN MODIFIED IN STAGING  AREA WHEREAS OTHER M DENOTES IT IS CHANGED IN WORKING AREA 

$ git status -s
MM NOTES.txt
 M about.html
M  contact.html

****************************************************************
****************************************************************

touch .gitignore
It create a file 
THAT WE DONT WANT TO SEND 
IT WILL ALSO DECREASE SPEED OF PUSH-PULL

CREATE A WASTE FILE THAT U WANT TO IGNORE LIKE 
(IT WILL IGNORE EVEN IF IT IS PRESENT IN SOME INSIDE FOLDER THEN ALSO)
mylogs.txt


Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git add -A

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git status -s
A  .gitignore
M  NOTES.txt
M  about.html
M  contact.html

SEE IT HAS IGNORED THE GIT FILES 

IF WE WANT TO IGNORE FILES WITH SOME EXTENSION LIKE THEN USE Like 
EXAMPLE:
*.txt -> ignore all text files

IF WE WANT TO JUST REMOVE FROM FOLDER NOT FROM ANYWHERE ELSE
THEN USE /mylogs.txt
Only at main tree where gitignore is 

To ignore a folder 
use 
FolderName/


****************************************************************
****************************************************************
BRANCHES
(LIKE IF U WORK FOR SOME PROJECT VERY VERY IMP)
(U CAN'T MESS)
(LIKE EDITING A RUNNING WEBSITE )

TO PREVENT THIS THINGS 
WE USE BRANCHES 
WE CREATE COPY AND WORK ON THE COPIES

master : Main Branch 
git branch feature1
IT WILL CREATE A BRANCH 

AND HOW TO KNOW WHICH BRANCH WE ARE AT :

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git branch feature1

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git branch
  feature1
* master -> MEANS WE ARE AT MASTER BRANCH 

****************************************************************
****************************************************************
git checkout feature1 => SWITCHED TO FEATURE1 BRANCH 

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git checkout feature1
Switched to branch 'feature1'
M       NOTES.txt

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (feature1)
$ git branch
* feature1
  master
****************************************************************
IF OUR  COMPANY LIKE NOW AFTER WE MAKE CHANGE THEN THEY WILL SAY TO MERGE NOW

****************************************************************
IF COMPANY SAYS NO LIKE U CAN GO BACK TO MASTER BY SAYING 

git checkout master : IT WILL MAKE U GO BACK 
BUT SUDDENLY IF COMPANY APPROVES THEN U CAN COME BACK BY JUST SAYING
git checkout feature1
****************************************************************
Now if u want To merge to master 
then first 
git checkout master

AND DO git merge feature1




LIKE THIS :
Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (feature1)
$ git checkout master
Switched to branch 'master'

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git checkout feature1
Switched to branch 'feature1'

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (feature1)
$ git status
On branch feature1
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   NOTES.txt

no changes added to commit (use "git add" and/or "git commit -a")

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (feature1)
$ git branch
* feature1
  master

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (feature1)
$ git commit -a -m "ADDED BRANCH FEATURE"
[feature1 80694e9] ADDED BRANCH FEATURE
 1 file changed, 8 insertions(+), 2 deletions(-)

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (feature1)
$ git status
On branch feature1
nothing to commit, working tree clean

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (feature1)
$ git checkout master
Switched to branch 'master'

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git merge feature1
Updating 63c1206..80694e9
Fast-forward
 NOTES.txt | 38 ++++++++++++++++++++++++++++++++++++++
 1 file changed, 38 insertions(+)

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git log -1
commit 80694e97c5cb468b4836ab9710e4c29faafa0886 (HEAD -> master, feature1)
Author: Naman <a.naman@iitg.ac.in>
Date:   Fri Feb 18 12:34:10 2022 +0530

    ADDED BRANCH FEATURE

****************************************************************
IF WE WANT TO DIRECTLY CREATE AND GO TO THAT BRANCH WE USE 
git checkout -b Feature2(instead of first creating and then checkout to that branch)

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (master)
$ git checkout -b feature2
Switched to a new branch 'feature2'

Dell@NAMAN MINGW64 ~/Desktop/GIT IN ONE VIDEO (feature2)
$ git branch
  feature1
* feature2
  master
****************************************************************
WE HAD TO ALWAYS BRANCH AND THEN CHANGE
****************************************************************
****************************************************************
Note add Info To Commit Message 
Not like normal 😅😂
****************************************************************
GITHUB : HOSTING REPOSITORY 
****************************************************************
****************************************************************
REMOTE REPOSITORY 

WE WILL MAKE A REMOTE REPOSITORY 
WE WILL PUSH OUR LOCAL REPOSITORY THERE

WE WILL ADD REMOTE 
REMOTE : A URL  WHERE WE WILL HOST OUR REPOSITORY 

git remote add origin https://github.com/Naman-72/Learning-Git.git

THIS WILL NAME URL as origin 
WE ARE CONNECTING OUR LOCAL REPOSITORY 

THEN WE WILL WRITE 
git remote : it will show origin 

git remote -v : it tell url 

git push origin master : push  to origin from master repository 
(IT WILL WRITE )

BUT INCASE U HAVEN'T MADE IT PUBLIC U MADE PRIVATE THEN IT MEANS THAT REPOSITORY DOESNOT EXIST 

SO GO TO SETTINGS > SSH AND GPG KEY
WE WILL GIVE ACCESS OF OUR GITHUB ACCOUNT TO COMPUTER 
WE WILL DEPLOY SSH KEY 
GO TO 
Generating a new SSH key and adding it to the ssh-agent
AND GET SSH KEY FROM THERE 
$ ssh-keygen -********-C "your_email@example.com"
LIKE THIS CHANGE IT TO THIS 
(*********** IS JUST FOR PRIVACY😂)
$ ssh-keygen -********-C "********@*******"



PASTE THIS IN GIT BASH AND NOW YES
AND GET THIS INFO IN DOC BELOW THE SSH KEY 
OR JUST DO 
$ eval "$(ssh-agent -s)"
WE WILL GET AGENT KEY PID 
AND THEN WRITE 
$ ssh-add ~/.ssh/id_ed*****

NOW GO TO SETTINGS >SSH AND GPG 
AND THEN JUST ADD  NEW SSH KEY 


COPY THE PUBLIC KEY CONTENT AND PASTE IN GIT
AND USE CAT COMMAND
cat ~/.ssh/id_ed*******.pub

Create new SSH KEY AND THEN 
NAME ANY TITLE 
And copy the text generated and paste in key 

ADD SSH KEY


NOW DO 
git remote set-url=ssh(url) instead of https
git push -u origin master 


U CAN PUSH OTHER BRANCHES ALSO
git checkout feature1
git push -u origin feature1


PULL REQUEST : IF SOMEONE WANT TO IMPROVE 
*****************************************************************
*****************************************************************
*****************************************************************
git push  : direct command to push at master 
*****************************************************************
making git clone 

(IF U WANT TO COPY YOUR FRIEND PROJECT LIKE)
create a new folder anywhere in computer 
then 
open git bash there 
COPY THE URL 
git clone url FOLDER_NAME
if just 
git clone url then same name as owner
*****************************************************************
THANK YOU FOR VIEWING MY NOTES 
CREDITS TO CODE WITH HARRY 
😁😀😃😄❤
DONT FORGET TO STAR 
⭐




