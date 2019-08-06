# Workflow 1a:  Create and Update My Repo

#### This is your checklist:
- [ ] Create a repo on GitHub (GH)
- [ ] Clone a repo
- [ ] Look at remotes
- [ ] Update a local repo from the remote (pull)
- [ ] Update a remote from local changes (push)
- [ ] Look at git history

---

## Step 0:  Configure user
REMINDER:  did you [configure the user name](https://github.com/reshamas/git-intro-workshop/blob/master/workflows/w_0_3_setup.md#step-1--configure-user-on-local-computer)?

## Step 1:  create a repo (on GitHub)
- Click on `+` next to your profile picture
- Select `New Repository`
- Repository name:  `gitclass`
- Description (optional):  `test project for git`
- `Public` repos are free
- Check box for `Initialize this repository with a README` :white_check_mark: :heavy_exclamation_mark:
- Select green button `Create repository`

## Step 2:  Let's add a couple of files
- Add a Markdown file:  `holiday.md`
  - add a line with an emoji
  - I added:  `Looking forward to the party :pizza: ! :smiley:_` :arrow_right: _Looking forward to the party :pizza: ! :smiley:_
  	- Here's the [Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet/) :octocat:  - commit file at end of page
  - commit file at end of page
- Add a Python file:  `hello.py`
  - add a line, the ubiquitous:  `print("Hello World")`
  - commit file at end of page
  - add a description for GitHub commit
  
**The usual workflow is to create a repo, clone it, create and edit all your files locally, and then push things to your repo. We're just creating files on github for a quick start!**

### Note: Ensure commit messages are meaningful.

<p>
<img src="../images/useless_commit.png" width="45%" height="45%" />
</p>


## Step 3: `clone` the repo from GitHub to our terminal

**Q:  What is cloning?**  
**A:  Making a copy of something.**

For git, it generally means making a local copy of a repository that's hosted somewhere else.

### Copy URL for cloning

Click on the green button for your forked GitHub repo, and ensure it is showing the url for **Clone with HTTPS**  (other option is "Clone with SSH").  Copy that URL.    <br> 
<img src="../images/github_clone_button.png" align="left" height="40" width="180" >   <br> <br>
    
>my example  
```text
https://github.com/spbail/gitclass.git
```

## Step 4:  go to working directory (your local terminal)
Go to your working directory  
>my example
```bash
cd /Users/sam/ds/gitsample
```
```bash
pwd
/Users/sam/ds/gitsample
```  

## Step 5:  clone the repo  
<kbd> git clone <url_name> </kbd> 
>my example
```bash
git clone https://github.com/spbail/gitclass.git
```
```bash
Cloning into 'gitclass'...
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
```

## Step 6:  `cd` into the repo
<kbd> cd <repo_name> </kbd>
>my example
```bash
cd gitclass 
```
	
**Quick detour: let's look at the .git directory in your repo!**

## Step 7:  look at remotes
**Q:  What is a remote?**  
**A:  **Remotes** are copies of a repo on another computer **(or on a service like GitHub)****

<kbd> git remote -v </kbd>
>my example
```bash
git remote -v
origin	https://github.com/spbail/gitclass.git (fetch)
origin	https://github.com/spbail/gitclass.git (push)
```

**Note 1:**  
* notice you have push and pull access  

**Note 2:**
* to remove a remote:  <kbd> git remote rm <remote_name> </kbd>

## Step 8:  update a local repo from a remote (pull)
This step copies changes from a remote repository to a local repository.  
:key:  Do this **before starting work in a repository so you have the most up-to-date-changes.**   
**Note:**  this is a good step to practice even though the first time you clone a repo it will already be up to date.   

- <kbd> git pull </kbd> 
- create `name.py` file on GitHub 
- <kbd> git pull </kbd> to sync repo

## Step 9:  update a remote repo with local changes (push)
This step copies syncs a remote repository with a local repository.  
:key:  We usually **don't make changes on master. We'll cover branches in the next section!**   

## Step 10:  create a file
<kbd> ls </kbd>  
<kbd> touch <file_name> </kbd>  
	
<kbd> touch mars.md </kbd>  

>my example
```bash
ls
touch mars.md
```
```bash
ls
total 8
-rw-r--r--  1   32 Nov 22 09:39 README.md
% touch mars.md
% ls
total 8
-rw-r--r--  1   32 Nov 22 09:39 README.md
-rw-r--r--  1    0 Nov 22 09:49 mars.md

	mars.md
```

---
# :arrow_right_hook: Git Workflow

## Git Flow 
| #     | Command                   | Step  | Description      |
|-------|---------------------------| -----|------------------|
|  1    | `git add <filename>`      | begin tracking a file | adds a change in the working directory to the staging area; tells Git that you want to include updates to a particular file in the next commit.  |    
|  2    | `git commit -m "message"` | log the change | changes are recorded in Git (interaction is with local repo) |  
|  3    | `git push`                | finalize the change | changes are pushed from Git (local, terminal) to GitHub (browser account, remote) | 
 
**Note:**  It is better to make many commits with smaller changes rather than of one commit with massive changes: small commits are easier to read and review.


## Step 11:  get status of repo
<kbd> git status </kbd>  
>my example
```bash
% git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	mars.md
nothing added to commit but untracked files present (use "git add" to track)
```
    
## Step 12:  add/stage a file
<kbd> git add <file_name> </kbd>   
	
>my example  
```bash
git add mars.md 
```

**Note:**  to `add` a file is to begin tracking it:  
- adds a change in the working directory to the staging area
- tells Git that you want to include updates to a particular file in the next commit

## Step 13:  get status of repo
<kbd> git status </kbd>  
>my example
```bash
% git status
On branch sam_wip
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   mars.md
```

## Step 14:  commit a file  
<kbd> git commit -m 'message' </kbd>  
	
>my example
```bash
git commit -m 'adding first planet'
```
	
```bash
% git commit -m 'adding first planet'
[master 3950dd9] adding first planet
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 mars.md
```
**Note:**  to `commit` a file is to "log the change":  
- changes are recorded in Git (interaction is with local repo)

## Step 15:  get status of repo
<kbd> git status </kbd>  
>my example
```bash
% git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   mars.md
```

## Step 19:  push changes to your remote repo
<kbd> git push </kbd>  
	
>my example
```bash
git push
```	

```bash
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 273 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/spbail/gitclass.git
 * [new branch]      master -> master
 ```
**Note:**  to `push` a "commit" is to "finalize the change":  
- changes are pushed from Git (local, terminal) to GitHub (browser account, remote)

## Final step
Look at new file on github!

---

# Git history

(Not that kind of history)

## What is a commit?
A commit is a snapshot of your files at a point in time that's associated with an author and a list of changes. You can see the list of all commits in your repository via the git log:
<kbd>git log</kbd>

>my example
```bash
git log
```

```bash
commit 13afc8e450045f80cf00633a438547091bcac4c1
Author: Sam Bail <samanthapbail@gmail.com>
Date:   Tue Aug 6 15:50:21 2019 -0400

    Create hello.py
```

Each commit has a **commit hash** (you'll see either the long or short version) that is used to identify that particular commit.

## git blame and git show

Sometimes you want to know who made changes to a particular line in a file. You can use `git blame <filename>` to see each line annotated with the commit hash and author:

```bash
git blame holiday.md 
```
```bash
fb319636 (Sam Bail 2019-08-06 15:50:02 -0400 1) Looking forward to the party :pizza: ! :smiley:
```

By using `git show <commit hash>` you can see all the changes associated with a specific commit:

```bash
git show fb319636
```
```bash
commit fb319636d437015d7893663df58fdef840b04b41
Author: Sam Bail <samanthapbail@gmail.com>
Date:   Tue Aug 6 15:50:02 2019 -0400

    Create holiday.md

diff --git a/holiday.md b/holiday.md
new file mode 100644
index 0000000..62404c4
--- /dev/null
+++ b/holiday.md
@@ -0,0 +1 @@
+Looking forward to the party :pizza: ! :smiley:
```
