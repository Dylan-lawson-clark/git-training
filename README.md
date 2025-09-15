# Git training repo to help the homies
_Very rough examples and explanations. Please do your owen research as well. There is always something new to learn_

Check what needs to be updated and/or pull the changes from the remote version of the branch you are currently on

### git fetch 
_You want to see what changes you'll be pulling into your branch_
- Tells you important stuff and updates meta data. 
	- Important to ensure you have the latest info from the repo. (New branches created, new changes pushed, etc.)
- If nothing is returned, nothing important to see.

Always run this before you do any git opperations. My opinion at least
```
git fetch
```

---

### git branch -r
_Lists all the branches on the remote_
- Check what branches are on the repo

```
git branch -r
```

---

### git branch 
_Lists all the local branches_
- Check what branches are on your local machine

This will list the branches on your machibne
```
git branch
```

This will create a new branch on your machine *Not linked to remote yet!*
```
git branch new_branch_name
```

This will create a branch and link it to a remote branch <--set-upstream>
```
git branch -u new_branch_name
```

---

### git checkout
_This will pull a specified branch to your local machine_
- Use this to get a branch from the repo so you can work on it

This will checkout a specific branch
```
git checkout example_branch
```

---

### git switch
_Switch between local branches_
- Use this to switch between branches you have already created or checked-out
```
git switch branch_name
```

---

### git pull 
_You are confident you want the changes in the branch_
- Does a "git fetch" and "git pull". Tells you if there is nothing to pull.
- Pulls the latest changes for the active branch from the remote repository

If there are changes in the same file on remote and locally, you will run into merge conflicts.
```
git pull
```

---

### git add 
_When you're getting your files ready for a commit, you add them to the staging area_
- Moves modified or new files from your working directory to the staging area, preparing them for the next commit

Run this when you have made changes, added, or removes files, and you want to add *ALL* of them to the staging area. 
```
git add .
```

run this when you want to add specific files to the staging area
```
git add app/example-file.php app/example-folder
```

---

### git commit 
_Creates a new commit in your local repo. Commited changes are *not* in the remote repo yet and so no one else can access them_
- Takes all staged changes and creates a new commit in your *local* repository with a commit message

Run this when you are ready to commit your changes to a new commit
```
git commit -m "My commit message"
```

Run this when you want to ammend your previous commit
```
git commit --amend
```

---

### git push 
_Pushes your local commits to the remote repository_
- Uploads your local commits to the remote repository, making them available to other collaborators

Run this when you want to push your changes to the remote
```
git push
```

Run this when you have not linked your branch to a branch on remote
```
git push -u origin branch_name
```
