# Git Reference Notes

[A)  Add, commit, push a file](#section-a)  
[B)  Deleting & copying (moving) files in Git](#section-b)  
[C)  Branches](#section-c)  


## <a name="section-a"></a>A)  Add, commit, push a file

#### 1. See what’s changed since the last commit / repo sync
`git status` shows files that have changed or are untracked  
`git diff [optional: filename]` shows the changes themselves

#### 2. “Stage” the things you want to include in your commit
This includes both files that have changed and new files you want to add.

`git add <file or directory>`

#### 3. Commit your changes and add a useful message

`git commit -m ‘message goes here’`

#### 4. Push to the origin repo
syntax:  
`git push <remote> <branch>`  
`git push origin master`

#### Adding, committing a file
>my example 
```
$ git status
$ git add test.txt                     # sets working copy to staged copy
$ git status
$ git commit -m "add a simple file"    # staged copy to revision history
$ git push origin master               # send it to (my forked) repo (branch = master)
```

--

## <a name="section-b"></a>B)  Deleting & copying (moving) files in Git

#### Important:  To Remove a File from the Repo
`git rm filename`  

#### Important:  To Rename or Move a File in the Repo
`git mv filename` 

#### List of Git commands
`git`

#### Git log
`git log`

--

## <a name="section-c"></a>C)  Branches


[Helpful Tutorial:  Using Branches on Git](https://www.atlassian.com/git/tutorials/using-branches)  

Why use branches?
 * independent line of development
 * think of them as a way to request a brand new working directory, staging area, and project history
 * in Git, branches are a part of your everyday development process. 
    * when you want to add a new feature or fix a bug—no matter how big or how small,  spawn a new branch to encapsulate your changes
    * this makes sure that unstable code is never committed to the main code base
    * it gives you the chance to clean up your feature’s history before merging it into the main branch

**Note:  'wip' = 'work in progress'**    

 * **List branches**  
    `$ git branch`
 * **Create a new branch**  
    `$ git branch reshama_wip`
 * **Navigate between branches**  
    `$ git checkout branchname`
 * **Create and switch to branch** (2 steps in 1 line)  
    `$ git checkout -b testbranch`

 * **Delete a branch** (safe delete; won't delete if there are unmerged changes)  
    `$ git branch -d reshama_wip`
 * **Delete a branch** (force delete; will delete even if branch has unmerged changes)  
    `$ git branch -D reshama_wip`


 * **Rename a branch** (whichever is the current one, be careful)  
    `$ git branch -m newone_wip`
 * **Rename a branch** (can specify oldname and newname)  
    `$ git branch -m <oldname> <newname>`


 * **Back to main branch**  
    `$ git checkout master`
 * **Merge branches** (will merge specified <branchname> into current branch)  
    `$ git merge <branchname>`

###Copy file/folder from one branch to current branch (`master`)

Run this from the branch where you want the file to end up:  
on:  `master` branch
```
git checkout branch_wip myfile.txt
```

####Copy directory from one branch to current branch (`master`)
on:  `master` branch
```
git checkout branch_wip myfolder/** 
```

