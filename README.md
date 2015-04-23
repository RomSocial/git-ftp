# git-ftp
## Setup for Ubuntu Git Ftp. 

The source, the python file came from https://github.com/ezyang/git-ftp

But the instructions provided did not work for me.

This is an attempt to make a config that would work for me.

## Procedure 
create bare git repo

install python

move post-receive to hooks subfolder of the git repo (not work directory)

make it executable

move ftpdata and git-ftp.py to git repo

### Setting up branches
change the branch name and ftp login credentials

add more branches if needed

change the condition in post-receive to work for all branches that have ftp link

### Troubleshooting
if something does not work - set permissions higher

log file post-receive.log is filled for each commit (in git repo)
