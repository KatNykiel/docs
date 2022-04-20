# Creating a git repository

One of the first things to do after installing Atom would be set up your workspace.

Atom uses **projects** to manage different workspaces. For example, you might have a project for [Bell](https://www.rcac.purdue.edu/compute/bell), another for [nanoHUB](https://nanohub.org/), and another for local runs.

## Creating a project
TODO: setting up Atom project from scratch (do a clean install)
Is it better to use git locally or on cluster? See if cluster is even an option

## Setting up a Git Repository
If you've never used Git before, it's a tool used for version control. Instead of only saving the most recent version of each file, Git can track its history.

```{attention} Why go through the hassle of Git? It's a fail safe - if testing code makes it break, or your files are wiped, Git can save the day
```

While this tutorial will focus on individual uses of Git, it's primary appeal is as a coding collaboration tool. To learn more about why Git is useful, see the explanation provided [here](https://www.practicaldatascience.org/html/git_and_github.html). In short, here's a few relevant terms useful to know
- **repository**: The location where all of your files and changes are stored. Rather than just a folder, think of it as a history of different states of your folder
- **stage**: After editing a file, you can *stage* the changes you made to indicate that you want them tracked. There are some changes which you don't want to track (passwords, API keys, large files)
- **commit**: To *commit* adds all of the staged changes to your repository, saving this state
- **push**: To tell your repository that this commit/series of commits is the most updated version of your code
- **pull**: To *pull* is to take the latest pushed commit and update your files to reflect these changes. While it doesn't have a huge meaning here, when working on teams it's essential for sharing code.

```{note} If you don't already have a GitHub account, you can create one [here](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjasK_F8qL3AhVuhHIEHea9BmkQFnoECAkQAQ&url=https%3A%2F%2Fgithub.com%2Fjoin&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk)
```

TODO: actually setting up Atom git repo from within Atom
