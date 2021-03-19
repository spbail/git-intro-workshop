# Workflow 1b: Branches in git

- [ ] Create a branch
- [ ] Switch to another branch
- [ ] Makes changes and push changes to GH from terminal
- [ ] Submit a pull request (PR) on GH

## :arrow_right_hook: Why use branches?
- **Branching** means you diverge from the main line (usually the "master" branch) of development and continue to do work without changing the main line, like "scratch paper" but for online coding.  
- Can work on different parts in the codebase, or "features" or "web page updates"
    - create a separate *history* for each new *feature*
- This is an interesting article on branches:  [Atlassian tutorial on branches](https://www.atlassian.com/git/tutorials/using-branches)


## Step 1:  list branches
<kbd> git branch </kbd>  
>my example
```git
git branch
* master
```
 
## Step 2:  create a working branch (or "feature branch")
<kbd> git branch <branch_name> </kbd>
	
>my example  
`git branch sam_wip`

**Note:** You can create a branch off of any branch, not just master. When creating a new branch, make sure you're branching off of the right thing! When working in shared repos, it's also good practice to go to master (or the feature branch you want to work off) and pull from the remote before branching. That way you're branching off of the latest status of the repo. 

## Step 3:  list branches
<kbd> git branch </kbd>  
>my example
```bash
git branch
* master
  sam_wip
```

## Step 4:  switch to working branch
<kbd> git checkout <branch_name> </kbd>  
>my example  
```bash
git checkout sam_wip
```

## Alternative (one-line) workflow for Steps 21 and 23:
<kbd> git checkout -b <branch_name> </kbd>

## Step 5:  create a new file
<kbd>  ls </kbd>  
<kbd> touch <file_name> </kbd>  
	
<kbd> touch mercury.md </kbd>  

>my example
```bash
ls
touch mercury.md
```
```bash
ls
total 8
-rw-r--r--  1   32 Nov 22 09:39 README.md
% touch mercury.md
% ls
total 8
-rw-r--r--  1   32 Nov 22 09:39 README.md
-rw-r--r--  1    0 Nov 22 09:49 mercury.md

	mercury.md
```

---
## Step 6: go through the git add/commit workflow
Use git add and commit to make a new "commit" for the mercury.md file.

## Step 7:  push changes to your 'working branch' 
<kbd> git push <remote_name> <branch_wip> </kbd>  
	
>my example
```bash
git push origin sam_wip
```	

```bash
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 273 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/spbail/gitclass.git
 * [new branch]      sam_wip -> sam_wip
 ```

## Step 8:  look at files on working branch (on GitHub)
- go to repo on GitHub
- toggle "Branch" dropdown to find our working branch
- confirm that new file is there!
	
## Step 9:  submit pull request (on GitHub)
Go to GitHub and refresh your browser.  
My url is:  https://github.com/spbail/gitclass  

Select green button "Compare and pull request"  
<img src="../images/pull_request_button.png" align="left" height="40">   <br> <br>

---

### Summary of Steps for using branches
<kbd> cd /Users/sam/ds/gitsample </kbd>  
<kbd>  pwd </kbd>   
<kbd> git clone https://github.com/spbail/gitclass.git </kbd>   
<kbd> cd gitclass </kbd>   
<kbd> git remote -v </kbd>  
<kbd> git pull </kbd>  
<kbd> git branch </kbd> <kbd> git branch sam_wip </kbd>  
<kbd> git branch </kbd> <kbd> git checkout sam_wip </kbd>  
<kbd>  ls </kbd>  
<kbd> touch mercury.md </kbd>  
<kbd>  ls </kbd>  
<kbd>  git status </kbd> <kbd>  git add mercury.md </kbd>  		  
<kbd>  git status </kbd> <kbd>  git commit -m 'adding second planet' </kbd>  		  
<kbd>  git status </kbd> <kbd>  git push origin sam_wip </kbd>  
