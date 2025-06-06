
# 📘 Git & GitHub Notes

## 🧭 Basic Terminal Commands

| Command        | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `cd`           | Change directory.                                                           |
| `mkdir`        | Create a new directory.                                                     |
| `ls`           | List files in the current folder.                                           |
| `ls -a`        | List **all** files including hidden files (e.g., `.git` folder).            |

## 🔧 Introduction to Git & GitHub

- **Git** is a **free**, **open-source**, **fast**, and **scalable** version control system.
- **GitHub** is a cloud platform that allows developers to host and manage code using Git.

## ⚙️ Installing Git

- Download Git: [https://git-scm.com/downloads/win](https://git-scm.com/downloads/win)
- Check Git version:  
  ```bash
  git --version
  ```

## 🔐 Git Configuration

Set up your identity:
```bash
git config user.name "Your Name"
git config user.email "your.email@example.com"
```

View configurations:
```bash
git config --list
```

## 🔄 Cloning & Checking Status

- Clone a remote repository:
  ```bash
  git clone <repository-url>
  ```
- Check current state of the working directory:
  ```bash
  git status
  ```

### Git Status Types:

| Status      | Meaning                                             |
|-------------|-----------------------------------------------------|
| Untracked   | New file not being tracked by Git.                 |
| Modified    | File has been edited.                              |
| Staged      | File is staged and ready for commit.               |
| Unmodified  | No changes made to the file.                       |

## ➕ Add & ✅ Commit

- Add specific file:
  ```bash
  git add <file-name>
  ```
- Add all changes:
  ```bash
  git add .
  ```
- Commit changes:
  ```bash
  git commit -m "Your commit message"
  ```

## 📤 Push to Remote

- Push code to main branch:
  ```bash
  git push origin main
  ```
- For future direct pushes (after first push):
  ```bash
  git push -u origin main
  ```

## 🏗️ Initialize Local Repository

1. Create folder and initialize Git:
   ```bash
   mkdir LocalRepo
   cd LocalRepo
   git init
   ```
2. Add project files like `index.html`, `style.css`.
3. Stage and commit:
   ```bash
   git add .
   git commit -m "Initial local commit"
   ```

## 🔗 Connecting to GitHub

1. Create a new repository on GitHub.
2. Connect local to remote:
   ```bash
   git remote add origin <repository-url>
   git remote -v     # To verify remote
   git branch -M main   # Rename branch to main
   git push -u origin main
   ```

## 🌿 Branching Commands

| Command                                | Description                            |
|----------------------------------------|----------------------------------------|
| `git branch`                           | List all branches                      |
| `git branch -M main`                   | Rename current branch to main          |
| `git checkout <branch-name>`           | Switch to another branch               |
| `git checkout -b <new-branch-name>`    | Create and switch to a new branch      |
| `git branch -d <branch-name>`          | Delete a branch                        |

## 🔀 Merging & Pull Requests

### Method 1: CLI Merge
```bash
git diff <branch-name>   # Check difference
git merge <branch-name>  # Merge into current branch
```

### Method 2: Pull Request (PR)
- Use GitHub UI to create PR for code review and merging.

## ⬇️ Pulling Changes

```bash
git pull origin main
```
- Fetches and updates the local repo from remote main branch.

## 🔙 Undoing Changes

### 1. Undo staged changes:
```bash
git reset <file-name>
git reset
```

### 2. Undo latest commit:
```bash
git reset HEAD~1
```

### 3. Undo to specific commit:
```bash
git reset <commit-hash>             # Soft reset
git reset --hard <commit-hash>      # Hard reset (removes changes)
```

## 🍴 Fork

- A **fork** is a personal copy of someone else's repository.
- Used for contributing or modifying code without affecting the original repository.
