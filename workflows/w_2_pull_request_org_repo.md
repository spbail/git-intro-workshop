# Workflow 2: Collaboration: Working with someone else's repo

When you collaborate with other people on their work (e.g. at work or for open source projects), you usually work with someone else's repo. In this workflow, you will learn

### In this workflow, you will learn how to:
1. Fork someone else's repo
2. Clone the forked repo
3. Add the original repo as a remote
4. Make changes to the repo
5. Open a pull request against the *original repo*
6. Make changes to the code in an open PR

## Step 1: Forking a repo (on GitHub)

**Forking** a repo means you're making a copy of the repo in your personal GitHub account. Instead of working directly on the original repo, you generally work on your own copy, then submit a PR against the original repo, and have your changes merged into the original repo at the end.

* Go to an existing repo, e.g. **https://github.com/spbail/test_repo/**
* Click the "Fork" button in the top right corner.
* That's it! You now have a copy of the test_repo in your GitHub account.

**I need a volunteer to demo this :) Create a new repo "collab_repo" in your account and share the URL with me!**

## Step 2: Clone the forked repo

* Go to the repo homepage **in your personal GitHub account**
* Click the green "Code" button to clone
* Navigate into the parent directory for your code and clone the repo:

```bash
cd ~/code
git clone https://github.com/<MY GITHUB USER>/test_repo.git
cd test_repo
```

## Step 3: Add the original repo as a remote

When working with a fork of someone else's repo, you want to make sure that your fork is in sync with the original repo. In order to do this, you need to tell Git where to find the original repo, i.e. add it as another **remote**.

Look at your current remotes to see that `origin` is set to **your** GitHub URL.

```bash
git remote -v
```

Go to **the original repo** and copy the URL under "Code" (either HTTPS or SSH).

Add the original repo as a remote. You can choose any name, but we usually refer to the original repo as the `upstream`:

```bash
git remote add upstream https://github.com/spbail/test_repo.git
```

**Again**, the URL is different if you're using SSH authentication.

Confirm that the remote has been set:

```bash
git remote -vvv
```

This will now allow you to interact with the code in the original repo, e.g. by explicitly pulling changes onto your `main` branch:

```bash
git pull upstream main
```

## Step 4: Make changes on a new working branch

Create a new branch with a somewhat useful name and the switch to it, e.g.

```bash
git branch sam/new_feature
git checkout sam/new_feature
```
Then make **a small change** to one of the existing files in the repo, or create new files. Up to you!

Follow the standard Git workflow to create a new commit with a useful commit message that describes your change:

```bash
git status
git add <your file>
git commit -m "Fixing the..."
```

And finally, push the branch to your repo:
```bash
git push origin sam/new_feature
```

## Step 5: Open a PR against the original repo

Once you're done making changes, you usually want to have them merged back into the original repo. In order to do this, you open a PR and let the owner of the original repo review and accept your changes:
- Go back to **your** repo homepage and open a PR from the branch you just pushed.
- On the PR page, make sure your branch is compared against **the main branch in the original repo**.
- Create the PR with a useful message.
- The original repo owner (that's me!) can now review and accept your changes to be merged into the original repo.

## Step 6: Make changes to code in an open PR
If you want to make changes to your code and update the PR with changes, you can simply make another local commit and push it to your branch:

- Make more changes to a file.
- Run the git add, commit, push to the branch workflow
- Refresh the PR to see that the changes have been pushed to the branch.
- Repeat this as often as you want to add changes to the PR. You don't need to push after every commit!
