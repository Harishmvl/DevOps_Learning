### Git Commands Documentation

This section provides a list of commonly used Git commands.

#### **Initialize a Repository**

```bash
git init
```
- Initializes a new Git repository in the current directory.

#### **Configuring Git**

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
- Sets up your name and email, which will be associated with your commits.

```bash
git config --global color.ui auto
```
- Enables colorized Git output for better readability.

#### **Working with Files in Git**

##### **Adding Files to Staging Area**

```bash
git add <file-or-directory>
```
- Stages a specific file or directory for commit.

```bash
git add .
```
- Stages all new and modified files in the current directory.

```bash
git add -A
```
- Stages all changes in the repository, including deletions.

##### **Checking the Status of Your Repository**

```bash
git status
```
- Displays the status of the working directory and staging area.

##### **Viewing Changes**

```bash
git diff
```
- Shows changes between the working directory and the staging area.

```bash
git diff --staged
```
- Shows changes between the staging area and the last commit.

##### **Committing Changes**

```bash
git commit -m "Your descriptive commit message"
```
- Records a snapshot of the staged changes with a message.

```bash
git commit -am "Your message"
```
- Stages and commits all tracked files in one step.

##### **Viewing Commit History**

```bash
git log
```
- Shows the commit history.

```bash
git log --oneline --graph --all
```
- Shows a condensed view of the commit history with a graphical representation.

#### **Branching and Merging**

##### **Creating and Switching Branches**

```bash
git branch <branch-name>
```
- Creates a new branch.

```bash
git checkout <branch-name>
```
- Switches to the specified branch.

```bash
git checkout -b <branch-name>
```
- Creates and switches to a new branch in one command.

##### **Merging Branches**

```bash
git merge <branch-name>
```
- Merges the specified branch into the current branch.

```bash
git merge <branch-name> --allow-unrelated-histories
```
- Merges branches with unrelated histories.

##### **Deleting Branches**

```bash
git branch -d <branch-name>
```
- Deletes a local branch.

```bash
git push origin --delete <branch-name>
```
- Deletes a remote branch.

#### **Pushing and Pulling Changes**

##### **Pushing to Remote**

```bash
git push origin <branch-name>
```
- Pushes the current branch to the remote repository.

##### **Pulling from Remote**

```bash
git pull
```
- Fetches and integrates changes from the remote repository into the current branch.

#### **Undoing Changes**

##### **Discard Changes in a File**

```bash
git checkout -- <file-name>
```
- Reverts changes in the specified file to the last commit.

##### **Unstage a File**

```bash
git reset <file-name>
```
- Removes a file from the staging area without changing the working directory.

##### **Revert a Commit**

```bash
git revert <commit-id>
```
- Creates a new commit that undoes the changes from a specified commit.

##### **Resetting Commits**

```bash
git reset --soft <commit-id>
```
- Resets the repository to a specific commit, keeping changes in the staging area.

```bash
git reset --hard <commit-id>
```
- Resets the repository to a specific commit, discarding all changes.

#### **Cloning and Forking**

##### **Cloning a Repository**

```bash
git clone <repository-url>
```
- Creates a copy of an existing remote repository.

##### **Forking and Working with Upstream**

```bash
git remote add upstream <repository-url>
```
- Adds an upstream repository to pull changes from.

```bash
git fetch upstream
git merge upstream/main
```
- Fetches and merges changes from the upstream repository.

#### **Stashing Changes**

```bash
git stash
```
- Temporarily saves changes that are not ready to commit.

```bash
git stash apply
```
- Re-applies the most recent stash.

```bash
git stash pop
```
- Re-applies and removes the most recent stash.

```bash
git stash list
```
- Lists all stashed changes.

#### **Tagging Commits**

```bash
git tag <tag-name>
```
- Creates a lightweight tag for the current commit.

```bash
git tag -a <tag-name> -m "Tag message"
```
- Creates an annotated tag with a message.

```bash
git push origin <tag-name>
```
- Pushes a tag to the remote repository.

#### **Viewing Remote Repositories**

```bash
git remote -v
```
- Displays the URLs of remote repositories.

```bash
git remote show origin
```
- Shows detailed information about the remote repository.

#### **Working with Submodules**

##### **Adding a Submodule**

```bash
git submodule add <repository-url> <path>
```
- Adds a submodule to the repository.

##### **Initializing and Updating Submodules**

```bash
git submodule init
git submodule update
```
- Initializes and updates submodules.

---

### File Operation Commands

This section provides a list of common file operation commands in a Unix-based shell (like macOS or Linux).

#### **Listing Files and Directories**

```bash
ls
```
- Lists files and directories in the current directory.

```bash
ls -a
```
- Lists all files, including hidden files (`.git`).

```bash
ls -l
```
- Lists files in long format, showing permissions, ownership, size, and modification date.

```bash
ls -lrta
```
- Lists all files with details, sorted by time, in reverse order, including hidden files.

#### **Navigating Directories**

```bash
cd <directory>
```
- Changes the current directory to the specified directory.

```bash
cd ..
```
- Moves up one directory level.

```bash
pwd
```
- Prints the current working directory.

#### **Creating and Removing Files**

```bash
touch <file-name>
```
- Creates an empty file or updates the timestamp of an existing file.

```bash
rm <file-name>
```
- Deletes the specified file.

```bash
rm -r <directory>
```
- Deletes a directory and its contents recursively.

#### **Copying and Moving Files**

```bash
cp <source> <destination>
```
- Copies a file from source to destination.

```bash
cp -r <source-directory> <destination-directory>
```
- Copies a directory and its contents.

```bash
mv <source> <destination>
```
- Moves a file or directory from source to destination.

#### **Creating and Removing Directories**

```bash
mkdir <directory-name>
```
- Creates a new directory.

```bash
rmdir <directory-name>
```
- Removes an empty directory.

#### **Viewing File Content**

```bash
cat <file-name>
```
- Displays the content of a file.

```bash
head <file-name>
```
- Displays the first 10 lines of a file.

```bash
tail <file-name>
```
- Displays the last 10 lines of a file.

```bash
less <file-name>
```
- Allows scrolling through a file's content page by page.

```bash
nano <file-name>
```
- Opens a file in the Nano text editor for editing.

```bash
vim <file-name>
```
- Opens a file in the Vim text editor for editing.

#### **File Permissions**

```bash
chmod <permissions> <file-name>
```
- Changes the permissions of a file or directory.

```bash
chown <owner>:<group> <file-name>
```
- Changes the ownership of a file or directory.

#### **Searching Files**

```bash
find <directory> -name <file-name>
```
- Searches for files by name within a directory and its subdirectories.

```bash
grep "<pattern>" <file-name>
```
- Searches for a text pattern within a file.

```bash
grep -r "<pattern>" <directory>
```
- Searches recursively for a text pattern within all files in a directory.
