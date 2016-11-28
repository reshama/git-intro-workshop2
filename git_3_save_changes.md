# Save Work
task:  end changes from local computer to GitHub repo (sync repos)

## Git Flow 
| #     | Command                   |  Description      |
|-------|---------------------------| ------------------|
|  1    | `git add <filename>`      |  adds a change in the working directory to the staging area; tells Git that you want to include updates to a particular file in the next commit.  |    
|  2    | `git commit -m "message"` | changes are recorded in Git |  
|  3    | `git push`                | changes are pushed from Git (local, terminal) to GitHub (browser account) | 
 


## Git:  add, commit and push a file

### `git add` a file
This sets a file for staging:  
`git add print_name.py`  

>my example  
```
~/git_work/starting_git  master ✗                                                 14m ◒  
▶ git add print_name.py
```



```git
▶ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   print_name.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	print_name.py~


~/git_work/starting_git  master ✗                                               17m ✚ ◒  
▶ 
```

### `git commit -m 'message'`

```bash
▶ git commit -m 'adding file that prints my name'
[master bfefcd3] adding file that prints my name
 1 file changed, 1 insertion(+)
 create mode 100644 print_name.py

~/git_work/starting_git  master ✗                                                  0m ◒  
▶ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	print_name.py~

nothing added to commit but untracked files present (use "git add" to track)

~/git_work/starting_git  master ✗                                                  0m ◒  
▶ 
```

### `git push` (push changes up to GitHub browser)

```bash
▶ git push
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 316 bytes | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local objects.
To https://github.com/reshama/starting_git.git
   2a119c3..bfefcd3  master -> master

```

Voila! Check out your forked repo on the browser and the `print_name.py` file should be there!
