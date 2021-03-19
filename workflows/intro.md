# Workflows

---

## Intro to Git and GitHub

### Git     --> [terminal]
Git is a system for (distributed) version control. It runs at the **command line on your local machine** and allows you to keep track of your files and modifications in a "repository". Behind the scenes, Git keeps track of all changes to your files in metadata that's stored in a .git subdirectory in any repository.

*Distributed* version control means you have not only local version control, but can also sync files to/with remote copies.

Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development.

### GitHub    -->  [browser]
GitHub is a **website** that allows you to upload your git respositories online. It allows you to have a backup of your files, has a visual interface to navigate your repos, and it allows other people to be able to view your repos. Alternatives to GitHub are BitBucket and GitLab (self-hosted system), but GitHub is by far the most commonly used service.

GitHub is a central place to store your repo, so others can clone it, push to it, and pull from it.

It also includes some very nice tools for software projects, like Markdown README rendering, issue tracker and wiki tools, and the ability to “fork” a project to make your own independent copy of it for development.

[Read more about GitHub in this TechCrunch article!](https://techcrunch.com/2012/07/14/what-exactly-is-github-anyway/)

**Note:** If you only want to have local version control, you don't need to use GitHub at all. But of course, having remote backups of your files, collaboration features, etc, is a great plus.

<p>
<img src="../images/git_github_difference.png" width="95%" height="95%" />
</p>



## Why it's good to know Git
- version control your code - easier to roll back changes
- backing up your code remotely
- can share your coding work publicly
- can collaborate with others on projects and review/control changes
- knowing version control lets you contribute to open source (these repos are public)

---
## Setup

### [Workflow 0.1](w_0_1_installs.md): software installations
- terminal access
- git 
- GitHub account
- editor

### [Workflow 0.2](w_0_2_ssh_keys.md): SSH keys setup (optional)
- create `ssh` keys
- add `ssh` key to GitHub

### [Workflow 0.3](w_0_3_setup.md): general setup
- configure user
- set up working directory

---

## [Workflow 1a](w_1a_create_update_myrepo.md): create & update your repo
- create repo on GitHub
  - add, update files on GitHub
- clone (copy) GH repo to local computer
  - look at remotes
  - add, update files at Git terminal and send changes up to GH
  - look at Git history
  
## [Workflow 1b](w_1b_branches.md): working with branches
- create a new feature branch
- make changes and merge them to a remote branch
- create a pull request

## [Workflow 2](w_2_pull_request_org_repo.md): fork & update an organization repo 
- fork/clone an organization's repo
- add updates and submit a pull request

## [Workflow 3](w_3_collaborating.md): add a collaborator to your repo and manage pull requests
- using the repo from Workflow 1, add a collaborator
- the collaborator will make updates to your repo and submit pull requests
- you will accept their pull requests
