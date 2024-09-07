# Git in the Real-time Projects
## Full Workflow from Snapshots to Collaboration
1. Introduction to Git
Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. It helps developers track changes in source code during software development, enabling collaboration and ensuring project history is maintained.
2. Creating a Snapshot
 Initializing a Repository. The first step in Git is initializing a new repository:
git init
This creates an empty Git repository in your project folder, setting up the `. git` directory where Git will track changes.
Staging Files: To take a snapshot of your project, you need to **stage** the files that you want to commit. Staging allows you to select specific files for your next commit.
git add file1.js: Stages a single file.
git add file1.js file2.js: Stages multiple files.
git add *.js: Stages files matching a pattern.
git add . : Stages the entire current directory and its content.
Viewing the Status
Before committing, it's important to check the status of your working directory:
git status: Shows a detailed report of all changes.
git status -s : Displays a short status report.

3. Committing the Staged Files
A commit is like taking a snapshot of your project. It’s essential to give descriptive messages to your commits so that later, you can understand what changes were made.
git commit -m "Your message here”: Commits staged files with a message.
git commit: Opens the default editor for writing a more detailed message.
Skipping the Staging Area
If you want to skip the staging area and directly commit modified files:
git commit -am "Message"

4. Managing Files in Git
Removing Files
To remove a file from your project and version control:
git rm file1.js: Removes the file from the working directory and staging area.
git rm --cached file1.js: Removes the file only from the staging area, but keeps it locally.
Renaming or Moving Files
git mv file1.js file1.txt: Renames or moves the file in the project.

5. Viewing Changes
Before committing, you might want to view the changes between the working directory, the index, and the last commit:
git diff: Shows unstaged changes.
git diff --staged: Shows changes that have been staged.
git diff --cached: Same as the staged option.

6. Viewing History
Git allows you to review the history of commits.
git log: Displays a complete history.
git log --oneline: Shows a summary of commits.
git log --reverse: Lists commits from the oldest to the newest.
To view specific commits:
git show [commit-hash]: Shows details about a particular commit.

7. Undoing Changes
Un-staging Files
To undo a `git add` operation:
git restore --staged file.js
Discarding Local Changes

If you want to discard local changes and reset to the last commit:
git restore file.js: Discards changes in the working directory for `file.js`.
To discard all local changes:
git restore .

8. Branching & Merging
Creating and Managing Branches
Branches allow you to work on different parts of a project simultaneously.
git branch bugfix: Creates a new branch.
git switch bugfix: Switches to the `bugfix` branch.
git branch -d bugfix: Deletes the branch after it has been merged.
Merging
Merging brings changes from one branch into another.
git merge bugfix: Merges the `bugfix` branch into the current branch.
git merge --no-ff bugfix: Ensures a merge commit is created, even if a fast-forward is possible.

9. Stashing
Stashing allows you to temporarily save uncommitted changes and switch branches without losing your work.
git stash: Stashes uncommitted changes.
git stash list: Shows a list of stashes.
git stash apply: Re-applies the latest stash.
10. Rewriting History
Resetting Commits
If you want to undo recent commits while keeping changes, you can use Git reset:
git reset --soft HEAD: Removes the last commit but keeps the changes staged.
git reset --hard HEAD: Removes the last commit and discards the changes.
Rebasing
Rebasing helps you reapply commits on top of another base commit.
git rebase master: Rebase the current branch onto the master branch.
Cherry-Picking
You can apply a specific commit from one branch to another:
git cherry-pick [commit-hash]

11. Collaboration
Cloning a Repository
To collaborate on an existing project, you first clone it:
git clone [url]: Creates a local copy of a remote repository.
Syncing with Remotes
To synchronize your local repository with a remote:
git fetch: Downloads commits and updates from the remote without merging.
git pull: Fetches and merges changes from the remote.
git push: Pushes your local commits to the remote repository.

12. Branching & Tags
Tagging
Tags are used to mark important points in a project’s history, such as releases.
git tag v1.0: Tags the last commit as `v1.0`.
git tag -d v1.0: Deletes a tag.
Sharing Branches and Tags
You can push branches and tags to remote repositories:
git push origin bugfix: Pushes the `bugfix` branch.
git push origin v1.0: Pushes the `v1.0` tag to the remote.

Cherry-picking
git checkout main
git fetch origin
git log
git cherry-pick <commit_hash>

git cherry-pick –continue
git push origin main

# Thank You!
