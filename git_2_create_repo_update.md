#Create a Repository on GitHub


##Step 1: Create a repo using GitHub (on web browser)
- Click on `+` next to your profile picture
- Select `New Repository`
- Repository name:  `starting_git`
- Description (optional):  `test project for git`
- `Public` repos are free
- Check box for `Initialize this repository with a README`
- Select green button `Create repository`

##Step 2:  Let's add a couple of files
- Add a Markdown file:  `holiday.md`
  - add a line with an emoji
  - I added:  _Looking forward to Thanksgiving :turkey: !_
- Add a Python file:  `hello.py`
  - add a line, the ubiquitous:  _Hello World!_
  
**Note:  add a meaningful commit message**  

##Step 3:  Add collaborators (if you would like to share)

- Settings / Collaborators
- add GitHub username

## Step 4:  Clone repo

### Select green button "Clone or download" and copy url

### Go to directory on local computer  
For me, it is: 
`/Users/reshamashaikh/git_work`  

>my example
```bash
~/git_work  master ✗                                                                  ◒  
▶ pwd
/Users/reshamashaikh/git_work
```

### Clone repo
`git clone https://github.com/reshama/starting_git.git`  

>my example  
```bash
~/git_work  master ✗                                                                  ◒  
▶ git clone https://github.com/reshama/starting_git.git
Cloning into 'starting_git'...
remote: Counting objects: 15, done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 15 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (15/15), done.
Checking connectivity... done.
```

### `cd` into cloned repo

```bash
▶ pwd
/Users/reshamashaikh/git_work/starting_git

▶ ls
total 0
drwxr-xr-x  7   238 Nov 14 11:29 data-science-from-scratch
drwxr-xr-x  6   204 Nov 14 11:48 starting_git

~/git_work  master ✗                                                                  ◒  
▶ cd starting_git 

~/git_work/starting_git  master ✔                                                    6m  
▶ 
```

### Check out the remote
Note:  
- a 'remote' is a copy of a repository
- notice you have push and pull access  

>my example  
```bash
▶ git remote -v
origin	https://github.com/reshama/starting_git.git (fetch)
origin	https://github.com/reshama/starting_git.git (push)
```

### We can 'pull' updates from GitHub version
```bash
▶ git pull
Already up-to-date.
```

##Step 5:  Make changes on local computer 

### Let's make a change on local computer and push changes up to GitHub
Use an editor of your choice to create a python file which will print your name.  
My file `print_name.py` contains the following line of code:  
```python
print("My name is Reshama")
```

```bash
~/git_work/starting_git  master ✔                                                   11m  
▶ emacs print_name.py

~/git_work/starting_git  master ✗                                                 11m ◒  
▶ python print_name.py 
Hello, my name is Reshama

~/git_work/starting_git  master ✗                                                 12m ◒  
▶ 
```

### We made a change!  How does git track it?
To see what changes have been made since last `git pull`, type `git status`  
```bash
▶ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	print_name.py

nothing added to commit but untracked files present (use "git add" to track)

~/git_work/starting_git  master ✗                                                 14m ◒  
▶ 
```


