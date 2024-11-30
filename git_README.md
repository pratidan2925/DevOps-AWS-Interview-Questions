# GIT 
#### 1. What  is Git ?
-What: A distributed version control system.
-Purpose: Manages and tracks changes in source code during software development.
-How: Provides commands for branching, merging, and tracking history. Developers can work independently and merge their changes into a shared repository.
#### 2.  What is GitHub ? 
-What: A web-based platform for version control and collaboration using Git.
-Purpose: Hosts Git repositories and provides tools for collaboration, issue tracking, and code review.
-How: Allows developers to create repositories, clone them, commit changes, open pull requests, and review code online. Integrates with --other tools and services for CI/CD.

#### 3. Difference between git and github





#### 4.  What is git workflow

Working directory - Modify files in your working directory
Staging area (Index) - Stage the files and add snapshots of them to your staging area
Git directory (Repository) - Perform a commit that stores the snapshots permanently to your Git directory. Checkout any existing version, make changes, stage them and commit.

#### 5.  Merge types in Git-
Merge in Git allows you to join two or more development work created using git branch into a single branch
Recursive-Git will select recursive as a default strategy when pulling or merging branches. The recursive strategy can detect and manage merges that involve renames, but it cannot use detected copies.
 Resolve- The resolve strategy uses a 3-way merge for resolving branches and can resolve only two HEADs using a 3-way merge algorithm. It is safe and fast and detects criss-cross merge ambiguities in detail.
Octopus- When two or more branches are passed, the octopus strategy is engaged, by default. Octopus refuses if the merge has conflicts that need manual resolution. The basic use of Octopus is to bundle feature branch HEADs that have similarities.
Ours- Our strategy resolves multiple branches, but the result is always that of the current branch HEAD. It ignores all changes from all other branches very effectively. It is intended to be used to replace an old history of side branches.
 Subtree-The subtree strategy is the modified version of the recursive strategy. For example, we merge A and B trees. When corresponding to a subtree of A, B is first modified to reflect the tree structure of A. The modification can be done to the shared ancestor tree of A and B.


#### 6.  How do you solve the merge conflict in git ?
There is now specific tool to solve merge conflicts .The conflict is solved by discussion between the developers who have created the merge request or the person who requested the merge at last.

#### 7.  Easy Difference Between `git merge` and `git rebase`
git merge  
Combines Branches:    - Merges changes from one branch into another.
How It Works:   - Creates a new merge commit that combines the histories of both branches.
   History:  - Keeps the complete history, including all individual commits and a new merge commit.
     Conflict Handling:   - Conflicts are resolved once during the merge process.
     Advantages:   - Shows a complete and true history of how branches were integrated.
     Disadvantages:   - Can create a cluttered commit history with many merge commits.
git rebase
  Reapplies Commits:   - Moves commits from one branch to the tip of another branch.
    How It Works:   - Rewrites the commit history to apply commits on top of the target branch.
    History:  - Creates a clean, linear history without merge commits.
     Conflict Handling:  Conflicts are resolved one by one at each commit during the rebase.
     Advantages:   - Produces a simpler, more linear commit history.
     Disadvantages:    - Changes commit hashes, which can cause issues if the branch is shared with others.
Key Differences
Commit History: - 
      git merge: Keeps a full history with merge commits.
      git rebase: Creates a linear history without merge commits. 
Conflict Resolution: 
      git merge: Resolve conflicts once during the merge.
      git rebase: Resolve conflicts at each commit during the rebase.
 Use Case: - 
       `git merge: Use when you want to preserve the full history.
       git rebase: Use when you want a clean, linear history.


#### 8. Git Branching Strategy -
           1. We are not allowing any developer to do direct changes into the main/master branch.
2. Developers/Devops have to create a feature branch while changing/adding new code.
3. After done with the changes in the feature branch developer/devops has to merge
his/her code changes in the master/main branch.
4. We are following the 4-eye principle while merging code changes.
5. We have to add INC ID, REQ ID or Change ID while creating a feature branch and
merge request ex. (INC0902324, REQ092348, CHG009823, STORY-6865).

#### 9. Git Stash-

If you are working on some changes and requirement get changed or your manager
asked you to work on another task.
Then you can temp hold your changes into git stash.
-git stash
-git stash apply
 -git stash list
 -git stash show


####  10 . Git clone Vs Git pull Vs Git Fork Vs git fetch Vs git Push
1. Git Clone
Purpose: Create a copy of an entire repository.
Usage: git clone <repository_url>
Effect: Downloads the repository from the remote server to your local machine and sets up the remote-tracking branches.
2. Git Pull
Purpose: Update your local repository with changes from the remote repository.
Usage: git pull
Effect: Fetches changes from the remote repository and merges them into your current branch.
3. Git Fork
Purpose: Create a personal copy of someone else's repository on your GitHub account.
Usage: Done via the GitHub web interface.
Effect: Creates a separate repository on your GitHub account where you can make changes independently.
4. Git Fetch
Purpose: Download changes from the remote repository without merging them.
Usage: git fetch
Effect: Updates the remote-tracking branches in your local repository, but does not modify your working directory or current branch.
5. Git Push
Purpose: Upload your local repository changes to the remote repository.
Usage: git push
Effect: Sends your committed changes to the remote repository, updating it with your changes.
Summary
Git Clone: Copy a repository from remote to local.
Git Pull: Fetch and merge changes from remote to local.
Git Fork: Create a personal copy of a repository on GitHub.
Git Fetch: Fetch changes from remote without merging.
Git Push: Send local changes to the remote repository.

####  11. git pull Vs Git fetch -

Git fetch cmd fetches all the changes from the remote repo to the local repo without bringing the changes into the working directory. Git pull on the other hand brings the copy of the remote directory changes into the working directory.


Git pull = Git fetch + Git merge

####  12. Git Rebase -

Rebasing is the process to reapply commits on the top of another base trip. It is used to apply a sequence of commits. Alternative to merge. Linear process of merging.

#### 13. Cherry Pick -

Cherry-picking in Git is for applying the same commit from one branch to another.
In case you made a mistake and committed a change into the wrong branch, but want to
avoid merging the whole branch. You can pick a specific commit and merge it.
14.   Hotfix/bugfix
A hotfix is an urgent and quick correction applied to a production system to address a critical issue or bug. It is characterized by:
Urgency: Immediate attention to fix a severe problem.
Scope: Minimal changes focused on resolving the specific issue.
Deployment: Directly deployed to the production environment, often with limited testing due to the urgency.
Hotfixes aim to quickly resolve issues that significantly impact users or system functionality, ensuring the system remains operational.
A bug fix is a correction made to the software to resolve a defect or issue identified during development, testing, or post-release. Key points include:
Routine: Part of the regular development process.
Testing: Goes through standard testing procedures to ensure it doesn't introduce new issues.
Scope: Can range from simple code changes to more complex modifications.
Bug fixes aim to improve software quality by resolving identified defects and are typically included in regular updates or releases.

#### 15. Git Hooks-
	
Git hooks are scripts that Git executed before or after events such as commit, push, and pull. These scripts allow you to customize and automate certain tasks in your Git workflow.
Git hooks are stored in the .git/hooks directory of your Git repository.

ex pre-commit, pre-push, post-push
#### 16. Git revert -

Git revert is a command in the Git that is used to create a new commit that undoes the changes
made by a previous commit. When you use git revert, Git will create a new commit.

#### 17. Git reset -

git reset is a powerful Git command used to undo changes in the working directory and staging area.
git reset --hard: Discards all changes in both the staging area and working directory.
git reset --soft: Keeps all changes in both the staging area and working directory.
git reset --mixed: Resets the staging area but keeps changes in the working directory.



#### 18. Git revert and Git reset
git revert and git reset are both Git commands used to undo changes, but they work in different ways and are used for different purposes. 
Key Differences
Commit History:
Git Revert: Keeps the commit history intact by creating a new commit that undoes changes.
Git Reset: Alters the commit history by moving the HEAD to a previous commit, which can rewrite the commit history depending on the mode used.
Usage Context:
Git Revert: Preferred for undoing changes in a shared repository because it maintains history and does not rewrite commits.
Git Reset: Useful for local changes and history rewriting but should be used cautiously in shared repositories.
Safety:
Git Revert: Safe for collaborative work as it does not change commit history.

#### 19. Git tags
Git tags are a way to mark specific points in a repository’s history as being important. They commonly mark release points (e.g., v1.0, v2.0). Tags are very useful for versioning software releases and maintaining a history of significant points in a project’s development.

#### 20. Merging in Git:
Merging in Git is the process of combining changes from two branches into a single branch. This is typically done to integrate new features, bug fixes, or updates from one branch into another, such as merging a feature branch into the main branch.
#### 21. How to get a commit ID ?
But using “ git log ” command
Git commands 
Git diff: shows the differences of files that have not yet been prepared.
git commit -a-m "commit message": Commits all tracked changes with a message.
git status: Displays the status of your working directory.
git add file path: Add file(s) to staging area.
git checkout -b branch_name: Create and switch to a new branch.  branch + switch
git checkout branch_name: Switch to an existing branch.
Git branch - see all branches present in 
git commit --amend: Modify the last commit.
git push origin branch_name: Push a branch to a remote.
git pull: Retrieves and merges remote changes.
git rebase -i: Interactively rebase, rewrite commit history.
Git Clone: Creates a local copy of a remote repository.
git merge: Merge branches.
git log --stat: Displays commit logs with statistics.
Git log --oneline : see changes or log with commit id 
 git stash: Changes to the stash for later.
git stash pop: Apply and remove hidden changes.
 git show commit_id: Displays details about a commit.
git reset HEAD-1: Undo the last commit, preserving the changes locally.
git format-patch-1 commit_id: Creates a patch file for a specific commit.
git apply patch_file_name: Applies changes to a patch file.
 git branch - branch_name: Forcibly remove a branch.
 git reset: Undo commits by moving the branch reference.
 git revert: Undo commits by creating a new commit.
 git cherry-pick commit_id: Applies changes to a specific commit.
 git branch: Lists branches.
git reset-hard: Resets everything to a previous commit, deleting all uncommitted changes.
git init - A git init command creates a new repository. It can be used to convert a folder to an empty git repo.
Git add . - to add all files that we edited or changed 
Git blame “file name” - see changes made


#### 22.  What is github action
GitHub Actions is a powerful tool provided by GitHub for automating software workflows directly within your GitHub repository. It allows you to build, test, and deploy your code right from GitHub, enabling Continuous Integration (CI) and Continuous Deployment (CD) pipelines without needing to rely on external CI/CD systems.
Use Cases for GitHub Actions:
Continuous Integration (CI): Automatically build and test your code on every push or pull request.
Continuous Deployment (CD): Deploy applications to various environments (e.g., staging, production) based on triggers like merge to main branch.
Automation: Perform routine tasks like versioning, release management, and notifications.
Community and Open Source: Encourage contributions and automate workflows for open-source projects.




#### #### 24. Difference between Git and SubVersion

#### #### 25. Head command in git

