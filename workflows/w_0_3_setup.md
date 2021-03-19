# Workflow 0.3: Local setup

In this step, you will configure some basic settings on your local computer in order to work with Git.

## Step 1:  Configure Git user (on local computer)

### Configure user name and email (lets Git know who you are)
Type the following commands in your terminal and replace with your name and email:
```bash
git config --global user.name "Firstname Lastname"
git config --global user.email "myname@email.com"
```

To verify these additions, type `git config --list` 

### Configure (terminal) editor of choice
This determines which editor Git uses by default to edit commit messages. We set it to use "Vim" on Mac OS (check out the link below for Windows options):

```bash
git config --global core.editor "vim"
```

Other editor options can be found in [Setting Up Git](http://swcarpentry.github.io/git-novice/02-setup/)

---

## Step 2: Create your working directory for Git repos

I generally put all repos in one directory called `code`. It's totally up to you how you organize your directories, but let's use the following structure for this workshop.

Navigate to your home directory, then create the directory for your Git repositories and for this workshop:
```bash
cd ~
mkdir code
```

Whenever I create a new repo or any kind of project, I usually do that in the `code` directory. Some people like to call it `repos` or something else.
