# GIT 

#### What are Git and GitHub?
- Git: Git is a distributed version control system that tracks changes to files and coordinates work among multiple contributors. It allows for efficient collaboration, branching, merging, and version history management.
- GitHub: GitHub is a web-based platform that provides hosting for Git repositories and collaboration features. It offers additional features like issue tracking, pull requests, and code review tools.

#### What is the difference between Git and GitHub?
Git is a version control system that manages and tracks changes to files locally on your computer. GitHub is a hosting service for Git repositories that provides a web-based interface, collaboration features, and remote repository hosting.

#### What is a Git repository? Name some popular Git hosting services.
A Git repository is a collection of files and directories along with the version history of those files. Popular Git hosting services include GitHub, GitLab, Bitbucket, and AWS CodeCommit.

#### What is a version control system? Mention its types.
A version control system (VCS) is a software tool that manages changes to files over time, allowing multiple contributors to work collaboratively on projects. Types of VCS include distributed VCS (e.g., Git, Mercurial) and centralized VCS (e.g., SVN, CVS).

#### What are the main differences between Git and SVN?
- Git is a distributed version control system, whereas SVN (Subversion) is a centralized version control system.
- Git allows for offline work, branching and merging are easier, and every developer has a full copy of the repository. SVN requires constant connection to a central server, branching and merging can be more complex, and developers work with a working copy.

#### What are the advantages of using GIT?
- Advantages of Git include:
- Distributed development model.
- Offline work capabilities.
- Fast branching and merging.
- Data integrity and checksums.
- Support for large projects and repositories.
- Ecosystem and community support.

#### What language is used in GIT?
Git itself is primarily written in C, but it includes scripts and utilities that use shell scripting (bash, sh) and Perl.

#### What are the advantages of Git over SVN?
- Advantages of Git over SVN include:
- Distributed architecture.
- Faster operations (branching, merging).
- Offline support.
- Efficient handling of large repositories.
- Better support for non-linear development workflows.

#### What is Git Bash?
Git Bash is a command line interface and terminal emulator for Git on Windows. It provides a Unix-like shell environment where Git commands can be executed.

#### What is the meaning of “Index” or “Staging Area” in GIT?
The "Index" or "Staging Area" in Git is a buffer between the working directory (where modified files reside) and the repository (where committed changes are stored). Files in the index are staged for the next commit.

#### What is tagging in Git?
Tagging in Git is the process of associating a meaningful label (tag) with a specific commit to mark it as a milestone, release point, or significant point in the project's history. Tags can be annotated (with messages) or lightweight (just a pointer to a commit).

#### What is forking in Git?
Forking in Git refers to creating a copy of a repository under your GitHub account. It allows you to freely experiment with changes without affecting the original repository. Forked repositories can later be merged back via pull requests.

#### What is the use of a Git clone?
Git clone is used to create a copy (clone) of an existing Git repository from a remote source (like GitHub or another Git hosting service). It copies all the files, commits, and history from the remote repository to your local machine.

#### What is the function of ‘git config’?
git config is used to set or get configuration variables for Git, such as user name, email, editor, and behavior settings. It can be used to configure global, local, or repository-specific settings.

#### What is the process for creating a repository in Git?
To create a Git repository, you initialize a new repository using git init command in the directory you want to version control. Alternatively, you can clone an existing repository using git clone <repository_url>.

#### What is cherry-pick in Git?
Cherry-pick in Git is the process of applying a specific commit from one branch onto another branch. It allows you to pick individual commits and apply them to your current branch without merging the entire branch.

#### What is origin in Git?
In Git, "origin" is the default name given to the remote

#### What is the git push command?
git push is a Git command used to upload local repository content to a remote repository. It transfers commits from your local branch to a branch on a remote repository (like GitHub or GitLab). Example: git push origin master
This command pushes the commits from your local master branch to the master branch on the remote repository named origin.

#### What is the git pull command?
- git pull is a Git command that fetches and downloads content from a remote repository and updates the local repository to match that content. It combines git fetch (downloads new data from a remote repository) and git merge (integrates changes into the current branch). - Example: git pull origin master
- This command fetches changes from the master branch on the origin remote repository and merges them into your current local branch.

#### What is the difference between git fetch and git pull?
- git fetch downloads new data from a remote repository but does not integrate any of the changes into your working files or current branch. It updates your remote-tracking branches (origin/master, for example).
- git pull fetches data from the remote repository and automatically merges it into your current branch. It is essentially a git fetch followed by a git merge.

#### Explain git checkout in Git.
- git checkout is used to switch branches or restore working tree files in Git. It updates the working directory to match the specified branch or commit.
- To switch branches: git checkout branch_name
- To create a new branch and switch to it: git checkout -b new_branch_name
- To discard changes in the working directory: git checkout -- file_name

#### What does git rebase do?
- git rebase is used to reapply commits on top of another base tip. It is primarily used to integrate changes from one branch into another by moving the entire branch to begin on the tip of another branch.
- git rebase master
- This command takes all the changes that were committed on the current branch and replays them on top of the master branch.

#### What is the difference between git rebase and git merge?
- git merge takes the contents of a source branch and integrates it with the target branch, creating a new commit on the target branch.
- git rebase moves the entire feature branch to begin on the tip of the target branch. It effectively rewrites the commit history by creating new commits for each commit in the original branch.

#### What is revert in Git?
- git revert is used to undo a previous commit by creating a new commit that undoes the changes from the previous commit. It is a safer way to undo changes than git reset because it doesn't alter the project history.
- git revert <commit_hash>

#### What is the difference between resetting and reverting?
- git reset moves the current branch tip backward to an earlier commit, which can alter the commit history. It is used to undo local changes or move to a different commit.
- git revert creates a new commit that undoes the changes from a previous commit, without altering the commit history. It's used to undo changes already pushed to a remote repository safely.

#### What is the difference between ‘git remote’ and ‘git clone’?
- git remote is used to manage a set of tracked repositories. It allows you to interact with remote repositories such as adding new connections or renaming existing ones.
- git clone creates a local copy of a remote repository. It copies all the files, branches, and commits from the remote repository to your local machine.

#### What is GIT stash?
- git stash temporary shelves (or stashes) changes you've made to your working directory so you can work on something else, and then come back and re-apply them later.
- git stash

#### What is GIT stash drop?
- git stash drop removes the most recently stashed changes from the stash list. If you want to drop a specific stash, you can provide its index.
- git stash drop

#### Why do we need branching in GIT?
Branching in Git allows multiple developers to work on different features or fixes simultaneously without interfering with each other. It enables isolation of work, experimentation with new ideas, and parallel development.

#### What is HEAD in Git, and how many HEADs can be created in a repository?
In Git, HEAD is a reference to the currently checked out commit (or branch). It is a pointer to the last commit of the currently checked out branch. Each repository has only one HEAD.

#### What is the regular way for branching in GIT?
- The regular way to create and switch to a new branch in Git involves using the git checkout command with the -b option.
- git checkout -b new_branch_name
- State a way to create a new branch in Git.
- Another way to create a new branch in Git is by using the git branch command followed by git checkout.
- git branch new_branch_name
-  git checkout new_branch_name

#### How do you define a ‘conflict’ in git?
A conflict in Git occurs when two branches have made changes to the same part of the same file, and Git cannot automatically determine which change to accept. Git marks the conflicted area in the file and requires manual resolution.

#### How to resolve a conflict in Git?
To resolve a conflict in Git, you need to manually edit the files to fix the conflicting changes, add the resolved files using git add, and then commit the merged result using git commit. After resolving conflicts, you can continue with git rebase --continue or git merge --continue.





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

- Working directory - Modify files in your working directory
- Staging area (Index) - Stage the files and add snapshots of them to your staging area
- Git directory (Repository) - Perform a commit that stores the snapshots permanently to your Git directory. Checkout any existing version, make changes, stage them and commit.

#### 5.  Merge types in Git-
- Merge in Git allows you to join two or more development work created using git branch into a single branch
- Recursive-Git will select recursive as a default strategy when pulling or merging branches. The recursive strategy can detect and manage merges that involve renames, but it cannot use detected copies.
 - **Resolve-** The resolve strategy uses a 3-way merge for resolving branches and can resolve only two HEADs using a 3-way merge algorithm. It is safe and fast and detects criss-cross merge ambiguities in detail.
- **Octopus-** When two or more branches are passed, the octopus strategy is engaged, by default. Octopus refuses if the merge has conflicts that need manual resolution. The basic use of Octopus is to bundle feature branch HEADs that have similarities.
- **Ours-** Our strategy resolves multiple branches, but the result is always that of the current branch HEAD. It ignores all changes from all other branches very effectively. It is intended to be used to replace an old history of side branches.
 - **Subtree-** The subtree strategy is the modified version of the recursive strategy. For example, we merge A and B trees. When corresponding to a subtree of A, B is first modified to reflect the tree structure of A. The modification can be done to the shared ancestor tree of A and B.


#### 6.  How do you solve the merge conflict in git ?
There is now specific tool to solve merge conflicts .The conflict is solved by discussion between the developers who have created the merge request or the person who requested the merge at last.

#### 7.  Easy Difference Between `git merge` and `git rebase`
- **git merge**
  - Combines Branches: Merges changes from one branch into another.
  - How It Works: Creates a new merge commit that combines the histories of both branches.
  - History: Keeps the complete history, including all individual commits and a new merge commit.
  - Conflict Handling: Conflicts are resolved once during the merge process.
  - Advantages: Shows a complete and true history of how branches were integrated.
  -  Disadvantages:Can create a cluttered commit history with many merge commits.
- **git rebase**
    - Reapplies Commits: Moves commits from one branch to the tip of another branch.
    - How It Works: Rewrites the commit history to apply commits on top of the target branch.
    - History:  Creates a clean, linear history without merge commits.
    - Conflict Handling:  Conflicts are resolved one by one at each commit during the rebase.
    - Advantages: Produces a simpler, more linear commit history.
    - Disadvantages: Changes commit hashes, which can cause issues if the branch is shared with others.
- **Key Differences**
- Commit History: - 
   -   git merge: Keeps a full history with merge commits.
    -  git rebase: Creates a linear history without merge commits. 
-Conflict Resolution: 
     - git merge: Resolve conflicts once during the merge.
     - git rebase: Resolve conflicts at each commit during the rebase.
- Use Case: - 
     -  `git merge: Use when you want to preserve the full history.
     -  git rebase: Use when you want a clean, linear history.


#### 8. Git Branching Strategy -
- 1. We are not allowing any developer to do direct changes into the main/master branch.
- 2. Developers/Devops have to create a feature branch while changing/adding new code.
- 3. After done with the changes in the feature branch developer/devops has to merge
his/her code changes in the master/main branch.
- 4. We are following the 4-eye principle while merging code changes.
- 5. We have to add INC ID, REQ ID or Change ID while creating a feature branch and
merge request ex. (INC0902324, REQ092348, CHG009823, STORY-6865).

#### 9. Git Stash-

- If you are working on some changes and requirement get changed or your manager
asked you to work on another task.
Then you can temp hold your changes into git stash.
-git stash
-git stash apply
 -git stash list
 -git stash show


####  10 . Git clone Vs Git pull Vs Git Fork Vs git fetch Vs git Push
- **1. Git Clone**
-Purpose: Create a copy of an entire repository.
- Usage: git clone <repository_url>
- Effect: Downloads the repository from the remote server to your local machine and sets up the remote-tracking branches.
- **2. Git Pull**
- Purpose: Update your local repository with changes from the remote repository.
- Usage: git pull
- Effect: Fetches changes from the remote repository and merges them into your current branch.
- **3. Git Fork**
- Purpose: Create a personal copy of someone else's repository on your GitHub account.
- Usage: Done via the GitHub web interface.
- Effect: Creates a separate repository on your GitHub account where you can make changes independently.
- **4. Git Fetch**
- Purpose: Download changes from the remote repository without merging them.
- Usage: git fetch
- Effect: Updates the remote-tracking branches in your local repository, but does not modify your working directory or current branch.
- **5. Git Push**
- Purpose: Upload your local repository changes to the remote repository.
- Usage: git push
- Effect: Sends your committed changes to the remote repository, updating it with your changes.
- **Summary**
- Git Clone: Copy a repository from remote to local.
- Git Pull: Fetch and merge changes from remote to local.
- Git Fork: Create a personal copy of a repository on GitHub.
- Git Fetch: Fetch changes from remote without merging.
- Git Push: Send local changes to the remote repository.

####  11. git pull Vs Git fetch -

- Git fetch cmd fetches all the changes from the remote repo to the local repo without bringing the changes into the working directory. - Git pull on the other hand brings the copy of the remote directory changes into the working directory.


- Git pull = Git fetch + Git merge

####  12. Git Rebase -

Rebasing is the process to reapply commits on the top of another base trip. It is used to apply a sequence of commits. Alternative to merge. Linear process of merging.

#### 13. Cherry Pick -

Cherry-picking in Git is for applying the same commit from one branch to another.
In case you made a mistake and committed a change into the wrong branch, but want to
avoid merging the whole branch. You can pick a specific commit and merge it.

#### 14.   Hotfix/bugfix
- A hotfix is an urgent and quick correction applied to a production system to address a critical issue or bug. It is characterized by:
- Urgency: Immediate attention to fix a severe problem.
- Scope: Minimal changes focused on resolving the specific issue.
- Deployment: Directly deployed to the production environment, often with limited testing due to the urgency.
- Hotfixes aim to quickly resolve issues that significantly impact users or system functionality, ensuring the system remains operational.
- A bug fix is a correction made to the software to resolve a defect or issue identified during development, testing, or post-release. - - **Key points include:**
- Routine: Part of the regular development process.
- Testing: Goes through standard testing procedures to ensure it doesn't introduce new issues.
- Scope: Can range from simple code changes to more complex modifications.
- Bug fixes aim to improve software quality by resolving identified defects and are typically included in regular updates or releases.

#### 15. Git Hooks-
	
- Git hooks are scripts that Git executed before or after events such as commit, push, and pull. These scripts allow you to customize and automate certain tasks in your Git workflow.
- Git hooks are stored in the .git/hooks directory of your Git repository.

- ex pre-commit, pre-push, post-push
#### 16. Git revert -

Git revert is a command in the Git that is used to create a new commit that undoes the changes
made by a previous commit. When you use git revert, Git will create a new commit.

#### 17. Git reset -

- git reset is a powerful Git command used to undo changes in the working directory and staging area.
- git reset --hard: Discards all changes in both the staging area and working directory.
- git reset --soft: Keeps all changes in both the staging area and working directory.
- git reset --mixed: Resets the staging area but keeps changes in the working directory.



#### 18. Git revert and Git reset
- git revert and git reset are both Git commands used to undo changes, but they work in different ways and are used for different purposes. 
- **Key Differences**
**Commit History:**
- Git Revert: Keeps the commit history intact by creating a new commit that undoes changes.
- Git Reset: Alters the commit history by moving the HEAD to a previous commit, which can rewrite the commit history depending on the mode used.
**Usage Context:**
- Git Revert: Preferred for undoing changes in a shared repository because it maintains history and does not rewrite commits.
- Git Reset: Useful for local changes and history rewriting but should be used cautiously in shared repositories.
**Safety:**
- Git Revert: Safe for collaborative work as it does not change commit history.

#### 19. Git tags
Git tags are a way to mark specific points in a repository’s history as being important. They commonly mark release points (e.g., v1.0, v2.0). Tags are very useful for versioning software releases and maintaining a history of significant points in a project’s development.

#### 20. Merging in Git:
Merging in Git is the process of combining changes from two branches into a single branch. This is typically done to integrate new features, bug fixes, or updates from one branch into another, such as merging a feature branch into the main branch.

#### 21. How to get a commit ID ?
But using “ git log ” command

#### Git commands 
- **Git diff:** shows the differences of files that have not yet been prepared.
- **git commit -a-m "commit message":** Commits all tracked changes with a message.
- **git status:** Displays the status of your working directory.
- **git add file path:** Add file(s) to staging area.
- **git checkout -b branch_name:** Create and switch to a new branch.  branch + switch
- **git checkout branch_name:** Switch to an existing branch.
- **Git branch** - see all branches present in 
- **git commit --amend:** Modify the last commit.
- **git push origin branch_name:** Push a branch to a remote.
- **git pull:** Retrieves and merges remote changes.
- **git rebase -i:** Interactively rebase, rewrite commit history.
- **Git Clone:** Creates a local copy of a remote repository.
- **git merge:** Merge branches.
- **git log --stat:** Displays commit logs with statistics.
- **Git log --oneline :** see changes or log with commit id 
-  **git stash:** Changes to the stash for later.
- **git stash pop:** Apply and remove hidden changes.
-  **git show commit_id:** Displays details about a commit.
- **git reset HEAD-1:** Undo the last commit, preserving the changes locally.
- **git format-patch-1 commit_id:** Creates a patch file for a specific commit.
- **git apply patch_file_name:** Applies changes to a patch file.
-  **git branch - branch_name:** Forcibly remove a branch.
-  **git reset:** Undo commits by moving the branch reference.
-  **git revert:** Undo commits by creating a new commit.
-  **git cherry-pick commit_id:** Applies changes to a specific commit.
-  **git branch:** Lists branches.
- **git reset-hard:** Resets everything to a previous commit, deleting all uncommitted changes.
- **git init** - A git init command creates a new repository. It can be used to convert a folder to an empty git repo.
- **Git add .** - to add all files that we edited or changed 
- **Git blame “file name”** - see changes made


#### 22.  What is github action
- GitHub Actions is a powerful tool provided by GitHub for automating software workflows directly within your GitHub repository. It allows you to build, test, and deploy your code right from GitHub, enabling Continuous Integration (CI) and Continuous Deployment (CD) pipelines without needing to rely on external CI/CD systems.
- **Use Cases for GitHub Actions:**
- **Continuous Integration (CI):** Automatically build and test your code on every push or pull request.
- **Continuous Deployment (CD):** Deploy applications to various environments (e.g., staging, production) based on triggers like merge to main branch.
- **Automation:** Perform routine tasks like versioning, release management, and notifications.
- **Community and Open Source:** Encourage contributions and automate workflows for open-source projects.


#### 5. How do you securely store credentials in GitHub?
Answer: To securely store credentials in GitHub, I use GitHub Secrets, which are encrypted environment variables that can be used in GitHub Actions workflows. Sensitive information like API keys or passwords should never be hardcoded in the repository.
Scenario: In one project, I stored AWS credentials as GitHub Secrets, which were then accessed securely in a GitHub Actions workflow to deploy resources to AWS.

#### 7. How is pull request approval managed in GitHub?
Answer: Pull request approval in GitHub is managed through the use of reviewers and branch protection rules. Reviewers are assigned to review the code changes, and approvals are required before the pull request can be merged. Branch protection rules can enforce requirements like mandatory code reviews and passing CI checks.
Scenario: In my team, we set up branch protection rules to require at least two approvals before merging any pull request to the main branch. This ensures code quality and prevents unreviewed changes from being deployed.

#### 11. What are some key features of GitHub?
- Answer: Key features of GitHub include:
- Version Control: GitHub provides robust Git-based version control for code repositories.
- Pull Requests: A collaborative feature that allows for code review and discussion before merging changes.
- Actions: GitHub's CI/CD service for automating workflows directly from the repository.
- Issues: A tracking system for bugs, enhancements, and project management.
- Wiki: A documentation platform within the repository.
- Security: Features like Dependabot, code scanning, and GitHub Secrets for securing the repository.
- Scenario: I use GitHub's pull request and issue tracking features extensively in my projects to manage code changes and track development progress.


#### 14. What is a GitHub workflow, and how is it used?
Answer: A GitHub workflow is an automated process defined in a YAML file within a GitHub repository. It is used to automate tasks such as building, testing, and deploying code. Workflows are triggered by events like pushes, pull requests, or on a schedule.
Scenario: I created a GitHub Actions workflow to automatically build and test a Node.js application on every pull request. The workflow ensured that only code passing all tests could be merged into the main branch.

#### 15. How do you handle merge conflicts in Git?
- Answer: To handle merge conflicts in Git, I first identify the conflicting files using git status. Then, I manually edit the conflicted files to resolve the conflicts, marking the resolution in the file. After resolving all conflicts, I add the files to the staging area and commit the changes.
- Scenario: During a project, I frequently encountered merge conflicts due to parallel development efforts. I resolved these conflicts by carefully reviewing the changes from both branches, ensuring that the final merged code was correct and functional.

#### 14. How do you handle merging branches in Git?
Answer: Merging branches in Git involves checking out the branch you want to merge into, usually main or master, and using git merge <branch-name> to combine the changes from the specified branch. If conflicts arise, they need to be resolved manually before committing the merge. I also use git rebase for a cleaner commit history when necessary.







#### How do you compare 2 commits in git?
Use the command git diff commit1 commit2 to view the differences between two commits. You can also use git log to find commit hashes and git diff to compare changes.

#### What is git rebase?
git rebase integrates changes from one branch into another by moving the entire branch to begin on the tip of another branch. It can be used to maintain a linear project history and apply changes on top of a different base commit.

#### Difference between git rebase and merge.
- git merge: Combines the histories of two branches, resulting in a merge commit that maintains the original branch structure.
- git rebase: Reapplies commits from one branch onto another, creating a linear history by integrating changes directly without a merge commit.
#### Suppose you have deleted a file in git history. How will you find the deleted file and how will you restore it? What commands will you use?
- Find Deleted File: Use git log --diff-filter=D --summary to find information about deleted files.
- Restore Deleted File: Use git checkout <commit> -- path/to/deleted/file to restore the file from a specific commit. Alternatively, use git restore --source=<commit> path/to/deleted/file if using Git 2.23 or newer.






#### What are some key features of GitHub?
Key features of GitHub include repository hosting, version control, collaboration tools (issues, pull requests, code reviews), CI/CD with GitHub Actions, project management tools (projects, milestones), and integrations with various third-party services.

#### How do you securely store credentials in GitHub?
Credentials should not be stored directly in GitHub repositories. Instead, use GitHub Secrets to store sensitive information securely. Secrets are encrypted and can be used in GitHub Actions workflows. Additionally, tools like Vault by HashiCorp can be integrated for managing secrets securely.

#### Where is the Jenkinsfile typically stored?
The Jenkinsfile, which defines the pipeline as code, is typically stored in the root directory of the repository. This allows Jenkins to automatically detect and execute the pipeline when changes are pushed to the repository.

#### How is pull request approval managed in GitHub?
Pull request approval in GitHub is managed using code review workflows. Collaborators review the changes, provide feedback, and approve or request changes. Protected branches can be configured to require a certain number of approvals before a pull request can be merged. Additionally, status checks and CI/CD integration can enforce passing tests before approval.

#### What is a GitHub workflow, and how is it used?
A GitHub workflow is an automated process defined in a YAML file within the .github/workflows directory of a repository. Workflows specify a series of jobs to be executed based on triggers such as push events, pull requests, or scheduled times. They are used to automate CI/CD pipelines, testing, deployments, and other tasks.

#### How do you handle merge conflicts in Git?
- To handle merge conflicts in Git, you can:
- Identify the files with conflicts using git status.
- Open the conflicted files and manually resolve the conflicts by choosing the correct code.
- Mark the conflicts as resolved using git add <file>.
- Complete the merge with git commit or git merge --continue.
- Alternatively, use tools like git mergetool for a graphical interface to resolve conflicts.

#### What is GIT stash?
Git stash temporarily shelves (or stashes) changes you've made to your working directory, allowing you to clean your working directory without committing your unfinished work. This is useful when you want to switch branches without committing incomplete changes.

#### What is a branching strategy?
A branching strategy is a set of guidelines and workflows that a development team follows to manage branches in a version control system. Common strategies include Git Flow, GitHub Flow, and trunk-based development, each with its own rules for creating, merging, and deleting branches.

#### What is the command to discard changes in the working dir?
- To discard changes in the working directory, you can use:
```
git checkout -- <file>
```
- or to discard all changes:
```
git reset --hard
```

#### How do you handle codes in Nexus satisfactorily?
- To handle code artifacts in Nexus:
- Use repository management best practices.
- Organize artifacts into appropriate repositories.
- Implement retention policies to clean up old or unused artifacts.
- Use versioning to manage different versions of artifacts.
- Set up access controls to ensure security.
#### How do you manage GITHUB roles?
- GitHub roles can be managed by:
- Using GitHub’s built-in role system (owner, collaborator, team member).
- Setting repository permissions (read, write, admin) for individual users or teams.
- Using branch protection rules to enforce required reviews and other policies.
- Using GitHub organizations to manage multiple repositories and teams.




#### What is the purpose of `.gitignore?
The .gitignore file specifies which files or directories should be ignored by Git version control. It helps prevent sensitive or unnecessary files, such as build artifacts or configuration files, from being included in commits and pushed to the repository.

#### How do git merge and git rebase differ?
- git merge: Combines changes from one branch into another, creating a new merge commit. It preserves the branch history.
- git rebase: Applies commits from one branch onto another, creating a linear history by rewriting commits. It results in a cleaner history but alters commit hashes.

#### How do git reset and git revert differ?
- git reset: Moves the current branch’s HEAD to a specified commit and can change the working directory and index. It’s used to discard commits or changes.
- git revert: Creates a new commit that undoes the changes introduced by a previous commit. It preserves history by adding a new commit rather than altering past commits.

#### How do git fetch and git pull differ?
- git fetch: Retrieves updates from a remote repository but does not merge them into the current branch. It updates the local copy of the remote branches.
- git pull: Fetches updates from a remote repository and merges them into the current branch, combining the fetch and merge actions.

#### How do you check the differences between two commits in Git?
- Use the command git diff <commit1> <commit2> to see the differences between two commits. You can also use git log to find commit hashes and then git diff to compare them.

#### How do you check the status of the working directory in Git?
Use the command git status to view the current status of the working directory and staging area, including untracked, modified, or staged files.

#### While you're in the middle of working on a feature when you realize you need to address an urgent bug fix that requires your immediate attention. How would you handle temporarily setting aside your current changes to focus on the bug fix without committing incomplete work?
You can use git stash to temporarily save your current changes without committing them. After resolving the urgent bug fix, you can return to your feature work by applying the stashed changes using git stash apply.




#### How do you uncommit the changes that have already been pushed to GitHub?
To uncommit changes that have already been pushed to GitHub, you can use:
```
git revert <commit_hash>
```
- This creates a new commit that undoes the changes. For more complex scenarios, you might need to use git reset and git push --force, but this can rewrite history and should be used with caution.

#### What is the difference between git pull and git fetch?
git fetch downloads new data from a remote repository but does not merge it into your working directory. git pull performs git fetch followed by git merge, integrating the fetched changes into your current branch.


#### 24. Difference between Git and SubVersion

#### #### 25. Head command in git

