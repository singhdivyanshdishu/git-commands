
# Git Commands Reference

This README provides a comprehensive reference for common Git commands used in version control.

## Git Version

To check the installed version of Git, use:
```bash
git --version
```

## Initialize a Git Repository

To initialize a new Git repository in your project directory, run:
```bash
git init
```

## Staging Changes

- To stage a specific file:
  ```bash
  git add filename
  ```

- To stage only the changed files:
  ```bash
  git add .
  ```

- To stage all files in the current directory:
  ```bash
  git add *
  ```

- To unstage a file:
  ```bash
  git reset filename
  ```

## Committing Changes

To commit staged changes with a message, use:
```bash
git commit -m "Your commit message"
```

To commit all changes in the current directory (including new files) with a message:
```bash
git commit -m "Your commit message"
```

You can repeat the staging and committing process as needed:
```bash
git add .                      # (to stage changes again)
git commit -m "Second commit"  # (note: fix any typos in your commit messages)
```

## Viewing Changes

- To see the status of your files (staged, unstaged, untracked):
  ```bash
  git status
  ```

- To view the changes made in the working directory:
  ```bash
  git diff
  ```

- To view changes between the last commit and the working directory:
  ```bash
  git diff --cached
  ```

- To view the commit history:
  ```bash
  git log
  ```

## Pushing Changes

To push your changes to the remote repository:
```bash
git push
```

## Branch Management

To rename the current branch to `main`, use:
```bash
git branch -M main
```

To create a new branch:
```bash
git branch new-branch-name
```

To switch to a different branch:
```bash
git checkout branch-name
```

To create and switch to a new branch in one command:
```bash
git checkout -b new-branch-name
```

## Merging Branches

To merge a branch into the current branch:
```bash
git merge branch-name
```

## Remote Repository

To add a remote repository, run:
```bash
git remote add origin <url>
```

To push changes to the `main` branch on the remote repository:
```bash
git push -u origin main
```

To fetch and merge changes from the remote repository:
```bash
git pull origin main
```

## Git LFS (Large File Storage)

Git LFS is an extension for managing large files in Git repositories. To use Git LFS:

1. **Install Git LFS** (if not already installed):
   ```bash
   git lfs install
   ```

2. **Track large files** (e.g., images, binaries):
   ```bash
   git lfs track "*.psd"
   ```

3. **Add and commit changes** as usual:
   ```bash
   git add .gitattributes
   git add filename.psd
   git commit -m "Add large file"
   ```

4. **Push changes** to the remote repository:
   ```bash
   git push
   ```

## Summary of Commands

| Command                          | Description                                      |
|----------------------------------|--------------------------------------------------|
| `git --version`                  | Check the installed version of Git               |
| `git init`                       | Initialize a new Git repository                  |
| `git add filename`              | Stage a specific file                             |
| `git add .`                      | Stage all changed files                           |
| `git add *`                      | Stage all files in the current directory         |
| `git reset filename`             | Unstage a specific file                           |
| `git commit -m "message"`       | Commit staged changes with a message             |
| `git commit -am "message"`      | Commit all changes with a message                |
| `git status`                     | Check the status of your files                   |
| `git diff`                       | View changes made in the working directory        |
| `git diff --cached`              | View changes between the last commit and staged changes |
| `git log`                        | View the commit history                           |
| `git push`                       | Push changes to the remote repository             |
| `git branch -M main`            | Rename the current branch to `main`              |
| `git branch new-branch-name`    | Create a new branch                              |
| `git checkout branch-name`      | Switch to a different branch                      |
| `git checkout -b new-branch-name` | Create and switch to a new branch                |
| `git merge branch-name`         | Merge a branch into the current branch           |
| `git remote add origin <url>`   | Add a remote repository                           |
| `git push -u origin main`       | Push changes to the `main` branch on remote      |
| `git pull origin main`          | Fetch and merge changes from the remote repository|
| `git lfs install`               | Install Git LFS                                  |
| `git lfs track "*.psd"`         | Track large files with Git LFS                   |

Feel free to customize the commands and descriptions as per your requirements!
