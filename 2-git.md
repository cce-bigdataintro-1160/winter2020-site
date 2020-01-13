# Version Control

### Objectives
* Learn what is a versioning system
* Why use git
* Create a repository and do your first commit
* Collaborate using git

### What is a versioning system
* Version control systems are a category of software tools that help a software team manage changes to code over time
* A few famous examples are: git, subversion, mercurial, CVS, Perforce and Clear Case
* Some of the main features are:
  * Full history of all changes
  * Traceability of all changes with user and time
  * Ability to revert changes
  * Availability of Branches that allow team members to work concurrently on same code
  * Availability of Tags that allow for management of software releases
  * Availability of Code revision 
  * Automation of build chains

* How do you currently collaborate in your work? What's the versioning system used there? Some friendlier version include Google Docs and Sharepoint

### Why git
* Git is a *distributed* versioning system created by Linus Torvalds, the creator of Linux
* Small and lightweight
* Free and open source
* Has all the features mentioned above: [About Git](https://git-scm.com/about/)

### Creating a repository and doing your first commit
* We'll now learn how to deal with git locally
* In order to use git we'll need to initialize a repository, add files to it and commit them
* To understand what's happening, we'll use the `status` and `log` commands 
* Finally we'll see how the checkout command allows us to navigate across commits
* Let's look for a few git commands

1. Create a directory called `my-first-repo`. 
2. Navigate to it and initialize a git repository with `git init`. Check it with `git status` 
3. Create the files `cleaner.py`, `processor.py`, `data.csv`, write a few lines in each. Check the `git status` 
4. Add one of those files to your staging area using `git add <filename>`. Check the `git status` 
5. Commit that file to git using `git commit -m "My commit message"`. Check the `git status`
6. Add a second of those files to your staging area. Commit that file to git with a different message. Check the `git status` 
7. Add the remaining files and commit with a different message. Check the `git status`
8. Use `git log` to visualize all we did
9. Use the command `git checkout <commit id>` on the previous commits. Check what happened to the files
10. Use the command `git checkout master` . Check what happened to the files

### Collaborate using git
* Git allows for collaboration through the use of remote repositories
* Remote repositories are accessible by multiple users that can synchronize to through the use of the pull and push commands
* Here are a some of the existing [Distributed Workflows](https://git-scm.com/book/en/v2/Distributed-Git-Distributed-Workflows) possible with git
* [GitHub](https://github.com/) is one of the most used git remote servers, allowing users not only to have shared repositories but to also collaborate using other tools like wikis, issue trackers and others
* We'll now learn how to synchronize our work with GitHub which will be our main point of collaboration for this course
* Let's look for a few git remote commands

1. Create a repository `git-notebook` in GitHub
2. Use the `git clone <repository url>` command to clone it locally.
3. In the cloned repository you must create, add and commit a file called `README.MD` following the steps from previous exercise!.
4. Push your changes to GitHub using the command `git push` after you commit.
5. Use GitHub UI in your browser to visualize the file
6. Use the GitHub UI to modify the file and commit it.
7. Use the command `git pull` to fetch the latest changes to your local machine

* We can also share an existing project directly from PyCharm into GitHub using the VCS >> Import into Version Control option

### Final notes on Version Control with Git
* Let's review what we've learned today
* GitHub hosts a majority of the Big Data projects, let's take a look at [scikit-learn](https://github.com/scikit-learn/scikit-learn) together
* GitHub will be the central piece of our homework collaboration, from this class on, the homework will be delivered through GitHub (and some minor parts through Slack)
* GitHub will also serve as a portfolio for our work and your final project
* If you feel like you're overwhelmed by git, there are two alternatives, using the GitHub UI or using a graphical tool (PyCharm has an embedded tool for it!). 

### Additional Exercises Material
* [Extra exercises](./2-git-exercises.md): Additional exercises to practice Git

### Recommended References
* [Git CheatSheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet) All git commands in a single cheatsheet
* [Git UI Tools](https://git-scm.com/downloads/guis/): A list of UI tools for git
* [Git Reference](https://git-scm.com/docs): A reference to all git commands
* [Troubleshooting for Windows users](https://help.github.com/en/articles/configuring-git-to-handle-line-endings) who receive a message about incompatible line endings (CLRF vs LF)

### Advanced exercises material
* [Git Branching](https://learngitbranching.js.org/): Learn what git does in a visual way with this website

[Back To Main Page](./index.md)