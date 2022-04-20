# Creating a git repository

One of the first things to do after installing Atom would be set up your workspace.

Atom uses **projects** to manage different workspaces. For example, you might have a project for [Bell](https://www.rcac.purdue.edu/compute/bell), another for [nanoHUB](https://nanohub.org/), and another for local runs.

## Creating a project
TODO: setting up Atom project from scratch (do a clean install)
Is it better to use git locally or on cluster? See if cluster is even an option

## Setting up a Git Repository
If you've never used Git before, it's essentially a tool used for version control. Instead of only saving the most recent version of each file, Git can track its history.

While this tutorial will focus on individual uses of Git, it's primary appeal is as a coding collaboration tool. To learn more about Git, a more thorough tutorial is provided [here](https://www.practicaldatascience.org/html/git_and_github.html). In short, here's a few relevant terms useful to know
- **repository**: The location where all of your files and changes are stored. Rather than just a folder, think of it as a history of different states of your folder
- **stage**: After editing a file, you can *stage* the changes you made to indicate that you want them tracked. There are some changes which you don't want to track (passwords, API keys, large files)
- **commit**: To *commit* adds all of the staged changes to your repository, saving this state; however, they won't be pushed to others using the same repository
- **push**: To tell your repository that this commit/series of commits is the most updated version of your code
- **pull**: To *pull* is to take the latest pushed commit and update your files to reflect these changes. While it doesn't have a huge meaning here, when working on teams it's essential for sharing code.

Why go through the hassle of Git?
- It's a *fail safe*. If you find out the past two days of experimental coding have messed up your project, you can easily revert
- 'Google docs'-like collaboration, where everything is tracked live, isn't well suited to coding
- Nearly all open-source code uses some form of Git. It's good to be familiar with it
- Dropbox/Drive are slower alternatives that force the user to manually merge teammates' versions

```{note} If you don't already have a GitHub account, you can create one here
```

TODO: actually setting up Atom git repo from within Atom
