# Full Stack Leasons
Github test and good pratices

###
<img src='./git.png' height=50 width=50>
# Github Commands

## Initial Config
´´´bash
git config --global user.email "your_email@example.com"
git config --global user.name "username"
´´´
## SSH Config (use Git bash)<br>

Verify if exists a key
´´´bash
ls -al ~/.ssh
´´´

Add a new key
´´´bash
ssh-keygen -t ed25519 -C "your_email@example.com"
´´´

Initialize the agent
´´´bash
eval "$(ssh-agent -s)"
´´´

Add ssh key to agent
´´´bash
ssh-add ~/.ssh/id_ed25519
´´´

Copy the ssh key
´´´bash
clip < ~/.ssh/id_ed25519.pub
´´´

Add this key in Github
´´´bash
Github -> Settings -> SSH and GPG keys -> New SSH key -> Past the key
Use a good title to you remember
´´´

Conection Test
´´´bash
ssh -T git@github.com -> yes
´´´

###

# Git Commands

´´´bash
Initialize a new repository in a new folder
git init
´´´

´´´bash
Show the current state from repository
git status
´´´´

´´´bash
Add the modified file to the index (staging area)
git add <filename ou . >
´´´

´´´bash
Remove all files from index (staging area)
git rm --cached <file> / git restore --staged <filename ou . >
´´´
´´´bash
List all local branchs that exists
git branch

List all remote branchs
git branch -r

List all local/remote branchs
git branch -a
´´´

´´´bash
Move to a specific branch
git checkout <branchname>
´´´

´´´bash
Create a new branch and enter on this branch
git checkout -b <branchname>

Delete a branch
git branch -D <branchname>
´´´
´´´bash
Create a commit with all modifications in the index with a message
git commit -m "<description>"

Discard the last commit keeping the changes in the index
git reset --soft HEAD~1
´´´

´´´bash
Send commits from local repository to remote repository
git push
´´´

´´´bash
Update the local repository with informations from remote repository
git fetch
´´´

´´´bash
Update the local repository with news updates from remote branch
git pull
´´´