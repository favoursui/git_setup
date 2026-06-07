# A SHORT INTRODUCTION TO GIT, GITHUB, AND SETUP GUIDE

## What is Version Control?

Version control is a system that records changes made to files over time. It allows developers to track modifications, collaborate with others, and restore previous versions of a project when necessary.

## Importance of Version Control

* Helps track changes made to files and projects.
* Keeps a history of development progress.
* Records when changes were made and who made them.
* Makes collaboration easier among team members.
* Allows developers to revert to previous versions if errors occur.

## What is Git?

Git is a free and open-source distributed version control system used by developers to track changes in their code and manage project history efficiently.

## What is GitHub?

GitHub is a cloud-based platform built around Git. It provides developers with tools to store repositories online, collaborate with others, review code, manage projects, and contribute to open-source software.

## Differences Between Git and GitHub

### Git

* A free and open-source version control system.
* Installed and used locally on a computer.
* Tracks changes in files and source code.

### GitHub

* A cloud-based hosting platform for Git repositories.
* Provides collaboration features such as pull requests, issues, and project management.
* Offers both free and paid plans.

# A Comprehensive Git and GitHub Setup Guide for Beginners

This guide explains how to configure Git and GitHub on your computer and make your first project push.

## Step 1: Create a GitHub Account

If you do not already have a GitHub account, create one at:

https://github.com

## Step 2: Check if Git is Installed

Open your terminal and run:

```bash
git --version
```

If Git is installed, the command will display the installed version.

If you receive a "git: command not found" message, install Git using:

```bash
sudo apt update
sudo apt install git
```

After installation, verify it again:

```bash
git --version
```

## Step 3: Configure Git

Set your GitHub username:

```bash
git config --global user.name "your_github_username"
```

Set your GitHub email address:

```bash
git config --global user.email "your_email@example.com"
```

Verify your configuration:

```bash
git config --list
```

## Step 4: Generate an SSH Key

Create a new SSH key:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Press Enter to accept the default file location.

Start the SSH agent:

```bash
eval "$(ssh-agent -s)"
```

Add your SSH key to the agent:

```bash
ssh-add ~/.ssh/id_ed25519
```

Display your public SSH key:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the entire output.

## Step 5: Add the SSH Key to GitHub

1. Log in to GitHub.
2. Click your profile picture in the top-right corner.
3. Select **Settings**.
4. Click **SSH and GPG Keys**.
5. Click **New SSH Key**.
6. Enter a title for the key (for example, "My Laptop").
7. Paste the copied public key into the Key field.
8. Click **Add SSH Key**.

Congratulations! Your GitHub account is now connected to your computer using SSH.

## Step 6: Test the SSH Connection

Run:

```bash
ssh -T git@github.com
```

If successful, you should see a welcome message from GitHub.

## Step 7: Create Your First Repository

Create a project folder:

```bash
mkdir git_setup
cd git_setup
```

Initialize Git:

```bash
git init
```

Create a README file:

```bash
touch README.md
```

Add the file:

```bash
git add .
```

Create your first commit:

```bash
git commit -m "Initial commit"
```

## Step 8: Connect to GitHub

Create a new repository on GitHub and copy its SSH URL.

Add it as a remote:

```bash
git remote add origin git@github.com:USERNAME/REPOSITORY_NAME.git
```

Verify the remote:

```bash
git remote -v
```

## Step 9: Push Your Project

Rename the default branch to main:

```bash
git branch -M main
```

Push your code:

```bash
git push -u origin main
```

Your project is now successfully uploaded to GitHub.

# Conclusion

Git and GitHub are essential tools for modern software development. Git helps you track and manage changes locally, while GitHub enables collaboration and cloud storage for your repositories. Learning these tools is one of the first steps toward becoming an effective software developer

