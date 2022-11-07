---
title: "Git"

date: 2022-11-07
url: /git/
categories:
  - Linux
  - Windows
tags:
  - Ubuntu
draft: false
---
### Introduction

GitHub is a cloud-hosted Git management tool. Git is _distributed_ version control, meaning the entire repository and history lives wherever you put it. People tend to use GitHub in their business or development workflow as a managed hosting solution for backups of their repositories. GitHub takes this even further by letting you connect with coworkers, friends, organizations, and more.

In this tutorial, you will learn how to take an existing project you are working on and push it, so it also exists on GitHub.

## Prerequisites

To initialize the repo and push it to GitHub you’ll need:

1.  A free GitHub Account
2.  `git` installed on your local machine

## Step 1 — Create a new GitHub Repo

Sign in to GitHub and [create a new empty repo](https://github.com/new). You can choose to either initialize a README or not. It doesn’t really matter because we’re just going to override everything in this remote repository anyways.

![Screenshot of the user interface to create a new repository on GitHub.](https://assets.digitalocean.com/articles/how-to-push-an-existing-project-to-github/new-github-repo.png)

**Warning:** Through the rest of this tutorial, we’ll assume your GitHub username is `sammy` and the repo you created is named `my-new-project`. It is important that you replace these placeholders with your actual username and repo name.

## Step 2 — Initialize Git in the project folder

From your terminal, run the following commands after navigating to the folder you would like to add.

### Initialize the Git Repo

Make sure you are in the root directory of the project you want to push to GitHub and run:

**Note:** If you already have an initialized Git repository, you can skip this command.

```
git init

```

This step creates a hidden `.git` directory in your project folder, which the `git` software recognizes and uses to store all the metadata and version history for the project.

### Add the files to Git index

```
git add -A

```

The `git add` command is used to tell git which files to include in a commit, and the `-A` (or `--all`) argument means “include all”.

### Commit Added Files

```
git commit -m 'Added my project'

```

The `git commit` command creates a new commit with all files that have been “added”. The `-m` (or `--message`) sets the _message_ that will be included alongside the commit, used for future reference to understand the commit. In this case, the message is: `'Added my project'`.

### Add a new remote origin

```
git remote add origin git@github.com:sammy/my-new-project.git

```

**Note:** Remember, you will need to replace the highlighted parts of the username and repo name with your own username and repo name.

In git, a “remote” refers to a remote version of the same repository, which is typically on a server somewhere _(in this case, GitHub)_. “origin” is the default name git gives to a remote server _(you can have multiple remotes)_ so `git remote add origin` is instructing git to add the URL of the default remote server for this repo.

### Push to GitHub

```
git push -u -f origin main

```

The `-u` (or `--set-upstream`) flag sets the remote `origin` as the _upstream_ reference. This allows you to later perform `git push` and `git pull` commands without having to specify an `origin` since we always want GitHub in this case.

The `-f` (or `--force`) flag stands for _force_. This will automatically overwrite everything in the remote directory. We’re using it here to overwrite the default README that GitHub automatically initialized.

**Note:** If you did not include the default README when creating the project on GitHub, the `-f` flag isn’t really necessary.

### All together

```
git init
git add -A
git commit -m 'Added my project'
git remote add origin git@github.com:sammy/my-new-project.git
git push -u -f origin main

```

## Conclusion

Now you are all set to track your code
