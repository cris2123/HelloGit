
## Git basics commands

-****

- **git init**: Initialize local git repositorie.

- **git add *filename***: Track specified filename on your local repositorie.

- **git add *.c**: Track all files inside your root directory with specific extension.

- **git add * ** : Track all files inside your root directory.

- **git clone *url_repositorie***: copy remote repositorie on local folder

- **git status**: Tells on which state are files on local repositorie.

- **git status -s**: Give status info in a short way.

- **git diff**: Use to see what have you changed but not yet staged (unstaged).

- **git diff --staged**: Tells you what've you staged that will go into your next commit.

- **git commit -m "Message"**:  Creates the commit of staged files.

- **git commit -a -m "Message"**: Stage all files and commit at the same time.

## Git advanced commands

-****

- **git rm *filename***: Delete filename from staging area. It removes the file from the working directory.

- **git rm *filename* --cached**: Delete filename from staging area but don delete the file from the working directory.

- **git log**: Tells you a history of commits to monitor your work.


## Git Branching and merging

-****

- **git checkout -b branch_name**: Change to another branch named branch_name. If branch does not exist create the branch.

**Note**: Is recommended that you have all changes commited on your working branch before change to another because git wont let you change it until you have commited all files. 
