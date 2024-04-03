# git version control

## What is version control?

Version control is a system that records changes to files or sets of files over time. 

It allows you to track modifications, revert to previous versions, and collaborate with others on the same codebase. 

Version control systems are essential in software development, enabling multiple developers to work on the same project simultaneously while maintaining a organized and efficient workflow.

**Benefits of Version Control:**
- Track Changes: Version control systems keep a detailed log of every modification made to the code, including who made the change, when it was made, and why it was made. This makes it easy to track down and fix bugs, or revert to a previous working version if necessary.

- Collaboration: Multiple developers can work on the same codebase concurrently without overwriting each other's changes. Version control systems provide mechanisms for merging changes from different contributors into a unified codebase.

- Backup and Recovery: Version control acts as a backup system, allowing you to recover lost or damaged files by reverting to a previous version.

- Branching and Merging: Version control systems enable developers to create separate branches for new features or experiments, and then merge those changes back into the main codebase once they are stable and tested.

- Release Management: With version control, you can tag specific versions of your codebase, making it easier to manage and deploy releases.

# git

Git is a distributed version control system that is widely used in software development.

It was created by Linus Torvalds in 2005 to manage the development of the Linux kernel, and has since become the de facto standard for version control in the industry.

**Key Git Concepts:**
- **Repository**: A repository (or "repo") is a collection of files and directories that Git tracks. It contains the complete history of changes made to the project over time.

- **Commit**: A commit is a snapshot of the repository at a particular point in time. Each commit records changes made to the files, along with a commit message describing the changes.

- **Branch**: A branch is an independent line of development within a repository. Branches allow you to work on new features or experiments without affecting the main codebase (often called the "main" or "master" branch).

- **Merge**: Merging is the process of combining changes from one branch into another. When you've completed work on a branch, you can merge it into the main branch to incorporate your changes.

- **Pull** Request: In collaborative environments, a pull request is a way to propose changes from your branch to be merged into the main codebase. Other team members can review the changes before they are merged.

## Basic git workflow

Here's a typical workflow when working with Git:

- **Clone**: Create a local copy of the repository on your machine using `git clone <repo_url>`.

- **Branch**: Create a new branch for your feature or bug fix using `git checkout -b <branch_name>`

- **Edit**: Make changes to the codebase and save the files.

- **Stage**: Stage the modified files for committing using `git add <file_names>`

- **Commit**: Record the changes with a commit message using `git commit -m "Descriptive commit message"`

- **Push**: Upload your commits to the remote repository using `git push origin <branch_name>`

- **Pull Request (optional)**: If you're working in a collaborative environment, create a pull request to propose your changes for review and merging.

- **Merge**: Once your changes are approved, merge your branch into the main branch using `git merge <branch_name>`

- **Pull**: Periodically update your local repository with the latest changes from the remote repository using `git pull`

**In BBI Class environment:**

Usually in your classes you will be running these commands only:

- `git add .` - to stage all changes

- `git commit -m "Your commit message here"` - to commit changes

- `git push` - to push changes to the remote repository