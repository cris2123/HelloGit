
## Git basics commands

-****

- **git init**: Initialize local git repositorie.

- **git add *filename***: Track specified filename on your local repositorie.

- **git add *.c**: Track all files inside your root directory with specific extension.

- **git add *** : Track all files inside your root directory.

- **git clone *url_repositorie***: copy remote repositorie on local folder

- **git status**: Tells on which state are files on local repositorie.

- **git status -s**: Give status info in a short way.

- **git diff**: Use to see what have you changed but not yet staged (unstaged).

- **git diff --staged**: Tells you what've you staged that will go into your next commit.

- **git commit -m "Message"**:  Creates the commit of staged files.

- **git commit -a -m "Message"**: Stage all files and commit at the same time.

## Git advanced commands
-****

- **git rm *filename***: Delete filename from staging area. It removes the file
from the working directory.

- **git rm *filename* --cached**: Delete filename from staging area but dont
 delete the file from the working directory.

- **git log**: Tells you a history of commits to monitor your work.


## Git branching and merging

-****

-**git merge branch_name**: Lets combine the work of the working branch with the
 specified branch.

- **git branch -d branch_name**: Remove specified branch.

- **git checkout -b branch_name**: Change to another branch named branch_name.
If branch does not exist create the branch.

**Note**: Is recommended that you have all changes commited on your working
branch before change to another because git wont let you change it until
you have commited all files.

**Note**: If git cannot do the merge automatically the best way is to make the
 merging manually. When that happen git put markers on conflicting files.  
 That markers are:

**>>>>>>>>>>**      
**==========**  
**<<<<<<<<<<**

**>>>>>>>>> FILENAME**  This tells that FILENAME is the master branch from where
we are making the merge.  

**=========** Lines code above this marker indicates what are the code lines of
the file of master branch.
The line codes of the branches files are at the bottom of this marker.

When we want to get the remote repo which could have diferents updates from what  
we have on our local repo , we need first stash our local changes to go back to a
clean version of work, then we do a git pull to bring the remote change to our local
repo and finally merge our stashed changes with the changes from the remote

- **``git stash``**
- **``git pull origin master``**
- **``git stash pop``**

If we have any conflict with our local changes and the remote ones we wold have to merge corrections manually, and then re commit changes to finish the process.

- **git stash**: Is used when you want to "save" the current state of the working directory and index, but want to go back to a clean working directory (to match
the HEAD commit )


## Git changing a remote's URL repositorie
-****

We can use git remote set-url  to change to which
remote we want to commit.

- **git remote set-url** *existing repo name*  *new_repo_link*

 - **existing repo name**: Name of a existing remote repo: upstream, origin are very common

 - **new repo link**: New URL for remote. Normally is something like this :
``https://github.com/USERNAME/OTHERREPOSITORY.git`` if you are using https

- **git remote -v**: Show me the remote to what we are
pushing.







**Note**: After the mergin process we need to stage the modified files and
make the commit.
