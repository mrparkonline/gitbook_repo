# Git & GitHub

[**Git**](https://git-scm.com/) and [**GitHub** ](https://github.com/)provide a robust version control system, facilitate collaboration and open-source development, offer backup and recovery mechanisms, and integrate with various tools to enhance the development workflow.

{% embed url="https://www.youtube.com/watch?v=USjZcfj8yxE" %}
Learn Git In 15 Minutes by Colt Steele
{% endembed %}

## What is Git?

Git is a distributed version control system that helps developers manage and track changes to their source code and other files.&#x20;

It allows multiple people to collaborate on projects, making it easier to work together, keep track of changes, and revert to previous states if needed. Git maintains a history of changes, making it possible to understand who made what changes and when. It's widely used in software development but can also be applied to other types of projects where version control and collaboration are important.

> ### Git Repository
>
> In version control systems, a repository is a data structure that stores metadata for a set of files or directory structure.
>
> By creating a repository, you are creating a `/.git` folder in your coding project space.
>
> By using git, the folder will contain all the changes that has been made throughout your code. The changes throughout your code will create a revision history that you can revert back to.

## What is GitHub?

GitHub is a web-based platform that uses the Git version control system to facilitate collaboration on software development projects. It provides tools for hosting repositories of code, managing changes through Git, and enabling multiple developers to work together on the same project. GitHub offers features like issue tracking, pull requests, code review, and project management, making it a popular platform for open-source and private software development. It allows developers to share, contribute to, and collaborate on code and projects with a global community.

{% hint style="info" %}
Some alternatives to GitHub:

* [GitLab](https://about.gitlab.com/)
* [Bitbucket](https://bitbucket.org/product)
* [Azure DevOps](https://azure.microsoft.com/en-ca/products/devops)
{% endhint %}

### How Git & GitHub helps a Development Project

1. Create a **"repository"** (project) with a git hosting tool.
2. Copy **(or clone)** the repository to your local machine
3. Add a file to your local repo and **"commit"** (save) the changes
4. **"Push"** your changes to your main branch
5. Make a change to your file with a git hosting tool and commit
6. **"Pull"** the changes to your local machine
7. Create a **"branch"** (version), make a change, commit the change
8. Open a **"pull request"** (propose changes to the main branch)
9. **"Merge"** your branch to the main branch

## Common Git Commands

1. **Initialization:**
   * Initialize a new repository: `git init`
   * Clone a repository: `git clone [repository URL]`
2. **Staging and Committing:**
   * Add changes to the staging area: `git add [file(s)]`
   * Commit staged changes: `git commit -m "Commit message"`
3. **Checking Status and Differences:**
   * View status of working directory: `git status`
   * Show changes between working directory and staging: `git diff`
   * Show changes between staging and last commit: `git diff --staged`
4. **Branches:**
   * List all branches: `git branch`
   * Create a new branch: `git branch [branch name]`
   * Switch to a branch: `git checkout [branch name]`
   * Create and switch to a new branch: `git checkout -b [branch name]`
   * Merge a branch into the current branch: `git merge [branch name]`
5. **Fetching and Pulling:**
   * Fetch changes from a remote repository: `git fetch`
   * Pull changes from a remote repository into the current branch: `git pull`
6. **Pushing:**
   * Push local changes to a remote repository: `git push [remote name] [branch name]`
7. **Remote Repositories:**
   * Add a remote repository: `git remote add [remote name] [repository URL]`
   * Remove a remote repository: `git remote remove [remote name]`
   * Show information about remotes: `git remote -v`
8. **Commit History and Logs:**
   * Show commit history: `git log`
   * Show a brief summary of commit history: `git log --oneline`
   * Show commit history for a specific file: `git log [file]`
9. **Undoing Changes:**
   * Discard changes in working directory: `git checkout -- [file]`
   * Unstage changes: `git restore --staged [file]`
   * Revert a commit: `git revert [commit hash]`
   * Delete untracked files: `git clean -f`
10. **Configuring Git:**
    * Configure user name: `git config --global user.name "Your Name"`
    * Configure user email: `git config --global user.email "your@example.com"`
