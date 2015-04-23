# git-ftp
## Setup for Ubuntu Git Ftp. 

create bare git repo
install python

move post-receive to hooks subfolder of the git repo (not work directory)
make it exacutable
move ftpdata and git-ftp.py to git repo

## Setting up branches
change the branch name and ftp login credentials
add more branches if needed
change the condition in post-receive to work for all branches that have ftp link

## Troubleshooting
if something does not work - set permissions higher
log file post-receive.log is filled for each commit (in git repo)
