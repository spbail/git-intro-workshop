# Workflow 1.2:  Pushing and pulling aka the Git workflow

### In this workflow, you will learn how to:
1. Update a local repo from a remote (pull)
2. Update a remote repo with local changes (push)

## Step 1:  Update a local repo from a remote (pull)

This step syncs changes from a *remote* repository to a *local* repository. This is usually important when you're collaborating with someone else and they might have made changes to files in the repo.

You usually do this **before starting work in a repository so you have the most up-to-date-changes.**   

**Note:**  This is a good step to practice even though the first time you clone a repo it will already be up to date.   

Let's do a small exercise to pretend someone has made changes to the repo content:
* Run `git pull` in your local repo.
* On GitHub, create a new file called `name.py` and add a `print('Hello Sam!')`
* In your local repo, run `git pull` to sync the new file to your machine.


## Step 2:  Update a remote repo with local changes (push)

This step syncs a remote repository with a local repository. We usually **don't make changes on the main branch. We'll cover branches in the next section!**   

**Let's create a new file and verify it's there: **
```bash
touch another_file.md
ls -lah
```

### Standard Git workflow

Your goal is to sync the changes to your local file back to GitHub. In order to do this, you generally follow the standard Git workflow of add, commit, push:

| #     | Command                   | Step  | Description      |
|-------|---------------------------| -----|------------------|
|  1    | `git add <filename>`      | Begin tracking a file | Adds a change in the working directory to the staging area; tells Git that you want to include updates to a particular file in the next commit.  |    
|  2    | `git commit -m "message"` | Log the change | Changes are recorded in Git (interaction is with local repo) |  
|  3    | `git push`                | Sync the change to the remote | Changes are pushed from Git (local, terminal) to GitHub (browser, remote) | 
 
**Note:**  
It is usually better to make many commits with smaller changes rather than of one commit with massive changes. Small commits are easier to read and review. **However** you might want to "squash" all your commits in the end to make sure the Git history isn't cluttered.

You could think of the stages that the files go through as a shopping workflow:
![Git workflow](../images/git_shopping_cart.png)

### Let's go through this workflow with our new file

Go through the git add, commit, push workflow, and make sure to check `git status` at each step to know what's going on:

```bash
git status
```

Then add the file to "stage" it to be committed. This tells Git that you want to include updates to the file in the next commit:

```bash
git add another_file.md 
```

Get the status again to see the status of the added file:

```bash
git status
```

Commit the file. To `commit` a file is to "log the change", i.e. they will be recorded in the Git history. Remember to add a useful commit message:

```bash
git commit -m 'Adding a new empty file'
```

Check the status of your repo to see that there are no unstaged files:

```bash
git status
```

You can also run `git log` to verify what your most recent (local) commit is:

```bash
git log
```

Finally, push your changes from your local machine to your remote repo (i.e. GitHub). **If you're using the HTTPS URL instead of SSH, GitHub will ask for your username and password**!

```bash
git push
```

You can now look at the new file on GitHub and verify that you pushed your commit!
