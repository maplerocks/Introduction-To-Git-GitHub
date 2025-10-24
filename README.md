# Getting Started with Git and GitHub

Here is a quick overview on GitHub Terminologies and Callable Methods. Use the Jump Links as you please:
1. [Common Terminologies](#10-Common-Terminologies)
2. [Command CheatSheet](#20-CheatSheet-For-Methods-And-Commands)
3. [Common Repo / GitHub Repo necesities](#30-Common-Repo-Setup)



## 1.0 Common Terminologies
Module 2 Glossary: 

Git Commands and Managing GitHub Projects
Welcome! This alphabetized glossary contains many of the terms in this course. This comprehensive glossary also includes additional industry-recognized terms not used in course videos. These terms are essential for you to recognize when working in the industry, participating in user groups, and in other professional certificate programs.

Estimated reading time: 4 minutes

| **Term** | **Definition** |
|-----------|----------------|
| **Cloning** | A process of creating a copy of the project's code and its complete version history from the remote repository on the local machine. |
| **Commit** | A snapshot of the project's current state at a specific point in time, along with a description of the changes made. |
| **Developer** | A computer programmer who is responsible for writing code. |
| **Distributed version control system (DVCS)** | A system that keeps track of changes to code, regardless of where it is stored. Multiple users work on the same codebase or repository, mirroring the codebase on their computers if needed, while the distributed version control software helps manage synchronization amongst the various codebase mirrors. |
| **Fork** | A copy of a repository into your GitHub account. |
| **Forking** | Forking creates a copy of a repository on which one can work without affecting the original repository. |
| **GitHub** | A web-hosted service for the Git repository. |
| **Git** | A free and open-source software distributed under the GNU General Public License. It is a distributed version control system that allows users to have a copy of their own project on their computer anywhere in the world. |
| **Integrator** | A role that is responsible for managing changes made by developers. |
| **Main branch** | A branch that stores the deployable version of your code. The main branch is created by default and is definitive. |
| **Merge** | A process to combine changes from one branch to another, typically merging a feature branch into the main branch. |
| **Origin** | A term that refers to the repository where a copy is cloned from. |
| **Pull request** | A process used to request that someone review and approve your changes before they become final. |
| **Remote repositories** | Repositories that are stored elsewhere. They can exist on the internet, on your network, or on your local computer. |
| **Repository administrator** | A role that is responsible for configuring and maintaining access to the repository. |
| **Repository** | A data structure for storing documents, including application source code. It contains the project folders that are set up for version control. |
| **Staging area** | An area where commits can be formatted and reviewed before completing the commit. |
| **Upstream** | A term used by developers to refer to the original source where the local copy was cloned from. |
| **Version control** | A system that allows you to keep track of changes to your documents. This process allows you to recover older versions of the documents if any mistakes are made. |


## 2.0 CheatSheet For Methods And Commands

| **Package/Method** | **Description** | **Code Example** |
|---------------------|-----------------|------------------|
| **git add** | Used to move changes from the working directory to the staging area | `git add sample.md` |
| **git add .** | Allows to move the changed files into the staging area on GitHub repositories | `git add .` |
| **git am** | Used to apply patches emailed to the repository | `git am < patchfile.patch >` |
| **git branch** | Allows to create an isolated environment within the repository to make changes | `git branch <new-branch>` |
| **git checkout** | Allows to see and change existing branches | `git checkout <existing-branch>` |
| **git checkout main** | Allows to switch to the main branch | `git checkout main` |
| **git clone** | Allows to create a copy of the remote repository | `git clone <repository-url>` |
| **git commit** | Allows you to take staged snapshots of changes and commit them to the project | `git commit -m "Your commit message here"` |
| **git config --global user.email / user.name** | Example 1: Sets a global email configuration for Git<br>Example 2: Sets a global username configuration for Git | Example 1:<br>`git config --global user.email "your.email@example.com"`<br><br>Example 2:<br>`git config --global user.name "Your Name"` |
| **git daemon** | Used to allow anonymous download from the repository | `git daemon --reuseaddr --verbose` |
| **git diff** | Helps others to review your code to identify and compare the changes | `git diff example.txt` |
| **git fetch** | Used to transfer the changes from the remote repo to your local repo | `git fetch <options> <remote name> <branch name>` |
| **git fetch upstream/main** | Used to grab upstream branches | `git fetch upstream main:upstream-main` |
| **git format-patch** | Generates or prepares e-mail submission if you adopt Linux kernel-style public forum workflow | `git format-patch -n <number_of_commits>` |
| **git http-backend** | Provides a server-side implementation of Git-over-HTTP, allowing both fetch and push services | ```bash\ngit clone --bare /path/to/repos/myrepo.git\ncd myrepo.git\ngit update-server-info\n``` |
| **git init** | Used to initialize a new Git repository | `git init <directory>` |
| **git instaweb** | Allows to set up web front-end to Git repositories | `git instaweb -p 8080` |
| **git log** | Enables browsing of previous changes to a project | `git log -p filename` |
| **git merge** | Used to merge changes in the active branch into another branch | `git merge feature_branch` |
| **git merge upstream/main** | Merges changes from the 'upstream/main' branch to the current branch | `git merge upstream/main` |
| **git pull** | Used to transfer the changes from the remote repo to your local repo, and merge them to a branch | `git pull origin main` |
| **git pull downstream** | Pulls changes from a downstream repository, specifically from the main branch of that repository | `git pull downstream main` |
| **git pull upstream** | Pulls changes from the "upstream" repository into the current branch | `git pull upstream main` |
| **git push** | Used to push all the committed changes into the repository | `git push origin your_branch_name` |
| **git remote** | A command to manage a set of tracked repositories | `git remote add upstream https://github.com/original/repo.git` |
| **git remote add origin** | Adds a remote repository named "origin" with the specified URL | `git remote add origin https://github.com/yourusername/your-repo.git` |
| **git remote add upstream** | Adds the original repository as a new remote repository labeled upstream | `git remote add upstream https://github.com/original/repo.git` |
| **git remote rename** | Renames a remote repository; first argument is the current name, second is the new name | `git remote rename origin new-origin` |
| **git remote -v** | Allows you to view the remotes associated with the local repository | `git remote -v` |
| **git request-pull** | Example 1: Creates a summary of changes for your upstream to pull<br>Example 2: Generates a summary of pending changes for an email request | Example 1:<br>`git request-pull origin/main your-branch`<br><br>Example 2:<br>`git request-pull <base> <head> <repository>` |
| **git rerere** | Reuses recorded resolution of previously resolved merge conflicts | ```bash\ngit rerere\ngit rerere diff\n``` |
| **git reset** | Undoes changes that were made to the files in your working directory | `git reset HEAD~1` |
| **git revert** | Used to undo botched commits | `git revert HEAD` |
| **git send-email** | Example 1: Sends your email submission without corruption by your MUA<br>Example 2: Sends a collection of patches as emails | Example 1:<br>```bash\ngit send-email --to=recipient@example.com\npath/to/patchfile.patch\n```<br><br>Example 2:<br>```bash\ngit send-email --to recipient@example.com\npatches/*.patch\n``` |
| **git-shell** | Used as a restricted login shell for shared central repository users | `sudo usermod -s /usr/bin/git-shell gituser` |
| **git status** | Allows you to see the state of your working directory and the staged snapshot of the changes | `git status` |
| **git version** | Displays the current Git version installed on your system | `git --version` |


## 3.0 Common Repo Setup
1. Readme.md
2. License.md
> License.md can be done in two ways.
> 1. Via GITHUB
> > This can be done either from the initial repo set up. Or later, by creating new File -> type "License" (A template button will appear) -> Select License Template.   
> 3. Via GIT CLI
3. Code of conduct
4. .gitignore
