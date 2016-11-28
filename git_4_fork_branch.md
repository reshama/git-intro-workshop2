# Fork & Clone a repo; use branches

### Go to repo on GitHub
In my personal account on GitHub, go to repo to be cloned.

In this example, it is:  https://github.com/joelgrus/data-science-from-scratch

### Fork repo
Upper right of github page:  "Fork" the repo

Go to my forked repo: https://github.com/reshama/data-science-from-scratch

 
### Clone repo
Clone that forked repo (which is now under my name)

In right column, find the link to **HTTPS clone URL** and **copy** that URL to be cloned.  
(Windows users may need to use ssh url.)  

### Go to working directory on local computer
```bash
▶ pwd
/Users/reshamashaikh

~  master ✗                                                                           ◒  
▶ mkdir git_work

~  master ✗                                                                           ◒  
▶ cd git_work

~/git_work  master ✗                                                                  ◒  
▶ pwd
/Users/reshamashaikh/git_work

~/git_work  master ✗                                                                  ◒  
▶ 
```



In terminal: 
* `cd` in to directory where repo will be cloned
* clone repo:   `git clone <url goes here>`
 - Example:  `git clone https://github.com/reshama/data-science-from-scratch.git`
* `cd` into cloned repo
```bash
▶ git clone https://github.com/reshama/data-science-from-scratch.git
Cloning into 'data-science-from-scratch'...
remote: Counting objects: 117, done.
remote: Total 117 (delta 0), reused 0 (delta 0), pack-reused 117
Receiving objects: 100% (117/117), 164.73 KiB | 0 bytes/s, done.
Resolving deltas: 100% (43/43), done.
Checking connectivity... done.
```

`cd` into clone repo:  
```bash
▶ ls
total 0
drwxr-xr-x  7   238 Nov 14 11:29 data-science-from-scratch

~/git_work  master ✗                                                                  ◒  
▶ cd data-science-from-scratch 

~/git_work/data-science-from-scratch  master ✔                                     498d  
▶ 
```

#### Check out the repo
```bash

~/git_work/data-science-from-scratch  master ✔                                     498d  
▶ ls
total 40
-rw-r--r--   1   1211 Nov 14 11:29 LICENSE
-rw-r--r--   1   3361 Nov 14 11:29 README.md
drwxr-xr-x  37   1258 Nov 14 11:29 code
-rw-r--r--   1   9600 Nov 14 11:29 links.md
```

#### List remotes
```bash
▶ git remote -v
origin	https://github.com/reshama/data-science-from-scratch.git (fetch)
origin	https://github.com/reshama/data-science-from-scratch.git (push)

~/git_work/data-science-from-scratch  master ✔                                     498d  
▶ 
```

### Create a branch
```bash
~/git_work/data-science-from-scratch  master ✔                                     498d  
▶ git branch
* master

~/git_work/data-science-from-scratch  master ✔                                     498d  
▶ git branch reshama_wip

~/git_work/data-science-from-scratch  master ✔                                     498d  
▶ git branch
* master
  reshama_wip

~/git_work/data-science-from-scratch  master ✔                                     498d  
▶ 
```

### Switch to working branch
```bash
~/git_work/data-science-from-scratch  master ✔                                     498d  
▶ git checkout reshama_wip
Switched to branch 'reshama_wip'

~/git_work/data-science-from-scratch  reshama_wip ✔                                498d  
▶ 
```

### Launch notebook from working branch (leave master branch intact)
```bash
~/git_work/data-science-from-scratch  reshama_wip ✔                                498d  
▶ jupyter notebook
```

---

###Copy file/folder from one branch to current branch (`master`)

Run this from the branch where you want the file to end up:  
on:  `master` branch
```
git checkout branch_wip myfile.txt
```

---

**Do this one time only**

`$ git config --global push.default simple`




