# git-ftp
## Git repositories

Bare git repo is the repository without working directory. It does not have the folder where the checkout files reside. It does not track any local folders for changes. You start the bare repo by adding --bare to git init or git clone command.

http://git-scm.com/book/en/v2/Git-on-the-Server-Getting-Git-on-a-Server

So, to make git server on one of your hostings - all you need is to create bare git repository there.

The best way to access it is with SSH - this way you can push, pull etc.

Others can do this too. So you can share code.

Bare repo, is very similar to .git directory that you have in the git tracked folder. Bare git repo often has a name, e.g. project.git - but it is still directory.

### Git + FTP

The source, the python file came from https://github.com/ezyang/git-ftp

The idea here is to be able to push to your git repository on server and allow git to update your FTP with new files. 

Only changed files are being transferred.

Git takes care of merging / conflicts.

But the instructions provided did not work for me. This is an attempt to make a config that would work most of the time.

### Install 

install python

create bare git repo

move post-receive to hooks subfolder of the bare git repo 

make it executable

move ftpdata and git-ftp.py to git repo

### Setting up branches
change the branch name and ftp login credentials

add more branches if needed

change the condition in post-receive hook to work for all branches that have ftp link

### Troubleshooting
if something does not work - set permissions higher

log file post-receive.log is filled for each commit (in git repo)

### Disclaimer

I'm no expert in scripts or Linux or git

It would be nice to improve this: I plan to figure out the needed permissions, explain the process of setting up specific user and giving proper permissions for this user, give all the commands for installing, as well as elaborate the local deployment commands (checkout specific branch to local folder).
