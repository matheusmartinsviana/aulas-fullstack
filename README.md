<img src='./git.png' height=50 width=50 />

# Github Commands 
This repository contains the basic commands to config your pc and how to use some commands on remote/local branchs. 🐱‍👤

###

# Github Commands

## Initial Config
```bash
git config --global user.email "your_email@example.com"
git config --global user.name "username"
```
## SSH Config (use Git bash)<br>

Verify if exists a key
```bash
ls -al ~/.ssh
```

Add a new key
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Initialize the agent
```bash
eval "$(ssh-agent -s)"
```

Add ssh key to agent
```bash
ssh-add ~/.ssh/id_ed25519
```

Copy the ssh key
```bash
clip < ~/.ssh/id_ed25519.pub
```

Add this key in Github
```bash
Github -> Settings -> SSH and GPG keys -> New SSH key -> Past the key
Use a good title to you remember
```

Conection Test
```bash
ssh -T git@github.com -> yes
```

###

# Git Commands

Initialize a new repository in a new folder
```bash
git init
```

Show the current state from repository
```bash
git status
```

Add the modified file to the index (staging area)
```bash
git add <filename ou . >
```

Remove all files from index (staging area)
```bash
git rm --cached <file> / git restore --staged <filename ou . >
```

List all local branchs that exists
```bash
git branch
```

List all remote branchs
```bash
git branch -r
```

List all local/remote branchs
```bash
git branch -a
```

Move to a specific branch
```bash
git checkout <branchname>
```

Create a new branch and enter on this branch
```bash
git checkout -b <branchname>
```

Delete a branch
```bash
git branch -D <branchname>
```

Create a commit with all modifications in the index with a message
```bash
git commit -m "<description>"
```

Discard the last commit keeping the changes in the index
```bash
git reset --soft HEAD~1
```

Send commits from local repository to remote repository
```bash
git push
```

Update the local repository with informations from remote repository
```bash
git fetch
```

Update the local repository with news updates from remote branch
```bash
git pull
```