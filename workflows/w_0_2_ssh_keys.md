# Workflow 0.2: SSH Setup for GitHub authentication (optional)

### Purpose
- ssh = Secure Shell, a network protocol that provides secure remote login from one computer to another.
- We can authenticate to GitHub in two ways: 1) Entering our username and password each time we interact with GitHub 2) Setting up permanent ssh authentication. 
- With SSH authentication you don't need to enter your credentials (GitHub username and password) each time you push a commit to the remote. 
  
**You can skip this step for now and complete it later after the course, but we recommend doing this.**

## Mac users

### Step 1:  Setup `ssh` keys (generate a key pair)

#### Step 1a:  Open terminal and go to your home directory

```bash
cd ~
pwd
```

#### Step 1b:  Go to `.ssh` directory
```bash
cd .ssh
```

**Note:**  If you do not have the `.ssh` directory, you can create it as follows: Go to your home directory, then type `mkdir .ssh`. This will create the directory. You can then run `cd .ssh` to go into the directory.


#### Step 1c: Generate `id_rsa` keypair files if needed

- **Note:**  These `id_rsa` files (`id_rsa` and `id_rsa.pub`) contain a special password for your computer to be connect to network services (Ex:  GitHub, AWS).
- Check to see if these files exist by typing `ls -la`
- If you do not have these two files (`id_rsa` and `id_rsa.pub`), create them by typing:  
	- `sh-keygen`
	- Press `enter` to confirm at each step (no passphrase needed, just press enter)

#### Step 1d: Copy `ssh` key to clipboard using `pbcopy` command
Run in your terminal:
`pbcopy < ~/.ssh/id_rsa.pub` 

Verify the key has been copied to the clipboard by printing the contents at your terminal: `pbpaste`

**Once you have copied your key, proceed to Step 2 below!**

---

## Windows Users

### Step 1: Follow this tutorial to create your SSH keys

[How to Create SSH Keys with PuTTY on Windows](https://www.digitalocean.com/docs/droplets/how-to/add-ssh-keys/create-with-putty/)


---

## Step 2 (for both Mac and Windows users):  Add `ssh` key to GitHub
- Go to your [GitHub account](https://github.com/) 
  	- Create one if you don't have one, and save your user name and password somewhere easily accessible for you.
- Click on your avatar/profile picture (upper right of screen)
- Go to `Settings`
- On left of screen, select `SSH and GPG keys`
- Select *New SSH key*
	- For *Title* enter "GitHub key"
	- For *Key* paste your `id_rsa.pub` key from clipboard here
- Click *Add SSH key*
- Save, exit, confirm GitHub password as requested


