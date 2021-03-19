# Brief intro to Git and GitHub

## Git 
Git is a system for (distributed) version control. It runs at the **command line on your local machine** and allows you to keep track of your files and modifications in a "repository". Behind the scenes, Git keeps track of all changes to your files in metadata that's stored in a .git subdirectory in any repository.

*Distributed* version control means you have not only local version control, but can also sync files to/with remote copies.

Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development.

## GitHub

GitHub is a **website** that allows you to upload your Git respositories online. It allows you to have a backup of your files, has a visual interface to navigate your repos, and it allows other people to be able to view your repos. There are alternatives to GitHub like BitBucket and GitLab, but GitHub is by far the most commonly used service.

GitHub is a central place to store your repo, so others can clone it, push to it, and pull from it.

It also includes some very nice tools for software projects, like Markdown file rendering, issue tracker and wiki tools, and the ability to “fork” a project to make your own independent copy of it for development.

[Read more about GitHub in this TechCrunch article!](https://techcrunch.com/2012/07/14/what-exactly-is-github-anyway/)

**Note:** If you only want to have local version control, you don't need to use GitHub at all. But of course, having remote backups of your files, collaboration features, etc, is a great plus.

![Git vs GitHub](../images/git_github_difference.png)


## Why it's good to know Git

- Version control your code - easier to roll back changes
- Backing up your code remotely
- Can share your coding work publicly
- Can collaborate with others on projects and review/control changes
- Knowing version control lets you contribute to open source projects!


## Setup recap: let's make sure we've done all these steps!


#### Workflow 0.1:  [Software Installations](workflows/w_0_1_installs.md) (Required)

#### Workflow 0.2:  [SSH Keys](workflows/w_0_2_ssh_keys.md) (Optional)

#### Workflow 0.3:  [Setup](workflows/w_0_3_setup.md) (Required)

---

## Workshop workflows

#### Workflow 1.1: [Create & update your repo](workflows/w_1_1_create_inspect_myrepo.md)

#### Workflow 1.2: [Pushing and pulling aka the Git workflow](/workflows/w_1_2_git_workflow.md)

#### Workflow 1.3: [Working with branches](workflows/w_1_3_branches.md)

#### Workflow 2: [Collaboration: Working with someone else's repo](workflows/w_2_pull_request_org_repo.md)
