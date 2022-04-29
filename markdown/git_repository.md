# Creating a git repository

If you've never used Git before, it's a tool used for version control. Instead of only saving the most recent version of each file, Git can track its history.

```{attention} Why go through the hassle of Git?
It's a fail safe - if your code breaks something, or files become corrupted, Git can save the day
```

While this tutorial will focus on individual uses of Git, it's primary appeal is as a coding collaboration tool. To learn more about why Git is useful, see the explanation provided [here](https://www.practicaldatascience.org/html/git_and_github.html). In short, here's a few relevant terms useful to know
- **repository**: The location where all of your files and changes are stored. Rather than just a folder, think of it as a history of different states of your folder
- **stage**: After editing a file, you can *stage* the changes you made to indicate that you want them tracked. There are some changes which you don't want to track (passwords, API keys, large files)
- **commit**: To *commit* adds all of the staged changes to your repository, saving this state
- **push**: To tell your repository that this commit/series of commits is the most updated version of your code
- **pull**: To *pull* is to take the latest pushed commit and update your files to reflect these changes. While it doesn't have a huge meaning here, when working on teams it's essential for sharing code.

```{note} If you don't already have a GitHub account, you can create one [here](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjasK_F8qL3AhVuhHIEHea9BmkQFnoECAkQAQ&url=https%3A%2F%2Fgithub.com%2Fjoin&usg=AOvVaw0H9TK-nu7JfXaoNeNMgJEk)
```

## Setting up a Git Repository
In the last step, we created a new project called 'Gilbreth,' now we'll initialize a Git repository in this directory. Press `CTRL-SHIFT-8` to open the GitHub panel.

- Click 'Login' and continue
- Copy the OAuth token to Atom to login
- Click 'Initialize and publish on GitHub'
- Enter a repository name and set visibility (most likely private)

In addition, we want to set up the Git panel, which we open using `CTRL-SHIFT-9`.
- Enter your name and email address
- If you intend to use this login for all repositories, click 'Use for all repositories'

You should now see a panel with three sections: unstaged changes, staged changes, and commit message. This will keep track of the changes you make and allow you to push them to Git.

```{note} Any changes you don't with to track on Git can be untracked by creating a file named '.gitgnore' and adding these file names (i.e. test.py or outVASP)
```
Create the .gitignore file by selecting the 'Gilbreth' folder in the left pane and pressing ```a```, then type '.gitignore' and add whichever files names you don't want to track

We can now make an initial commit

- In the Git panel, press 'Stage All' to stage your changes (creating the .gitignore file)
- Add a Commit message in the text box below, describing the changes this commit contains
- Click 'Create detached commit'
- Click 'Publish' to set up a remote tracking branch

Congrats! You should be able to view your repository on GitHub, and have the system in place to stage, commit, and push your changes from within Atom.

```{note} Atom has some pretty cool integrations with Git. See which changes were made between commits, merge branch conflicts, easily switch between branches, etc.
```
