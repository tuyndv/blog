Installing xclip for copy to clipboard
wget http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
sudo rpm -Uvh epel-release*rpm
sudo yum -y install xclip

github - adding ssh key - use xclip in place of clip
xclip -sel clip < ~/.ssh/id_rsa.pub
https://help.github.com/articles/generating-ssh-keys


Enabling port for git (TCP 9418) in cpanel
Plugins > ConfigServer Security & Firewall
Firewall configuration
TCP_IN & TCP_OUT - 9418
TCP_OUT - 22
---------------
check if ssh is working fine
https://help.github.com/articles/error-permission-denied-publickey
http://unix.stackexchange.com/questions/48863/ssh-add-complains-could-not-open-a-connection-to-your-authentication-agent
ssh -vT git@github.com

ssh-add -l
Could not open a connection to your authentication agent
eval "$(ssh-agent)"
ssh-add -l
Error: Permission denied (publickey)
ss-add /path/to/key (id_rsa)
ssh-add -l
Add the id_rs.pub key to github account
ssh -vT git@github.com
Hi vinodpandey! You've successfully authenticated, but GitHub does not provide shell access.
---------------



Git in 15 minutes
http://try.github.com/levels/1/challenges/1

Branching Demo
http://pcottle.github.com/learnGitBranching/
http://pcottle.github.com/learnGitBranching/?demo
http://pcottle.github.io/learnGitBranching/index.html

GUI client
http://sourcetreeapp.com/


======================
Github 
=====================
git status
git commit -m "Comment text"
git branch
git remote -v
git pull
git push origin master
origin - remote branch
master - local branch

==

git add file_name
git commit -m "message"
git pull
git push origin master
===
Solving conflicts
------------------
git pull
- error message - conflict error in files
fix the local conflicts and files
commit the changes in files with conflict (git commit ..)
git push origin master
=========================



tagging
---------
show tags: 
git tag

create tags (annotated):
git tag -a v1.4 -m 'version 1.4'

push tags to remote server:
git push --tags

working on tag: 
git checkout <tag_name>


# Why does git merge a branch into itself?
```
Ref: http://stackoverflow.com/questions/31463025/why-does-git-merge-a-branch-into-itself

git pull --rebase
```





