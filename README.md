# Removing All Files From the Main Branch

This repository has had all files removed except for this README.

## Instructions: How to Delete All Files From the Main Branch

If you ever need to delete all files (except README.md or any other file you want to keep) from the main branch, you can do so locally and push the changes to GitHub. Below are step-by-step instructions and example commands.

### 1. Clone Your Repository

```sh
git clone https://github.com/readysetm/website-demo.git
cd website-demo
```

### 2. Check Out the Main Branch

```sh
git checkout main
```

### 3. Remove All Files and Folders Except `.git` and README.md

> To preserve this README, run:

```sh
find . -mindepth 1 -not -name '.git' -not -name 'README.md' -exec rm -rf {} +
```

If you want to delete EVERYTHING, including the README, just remove the exception from the command.

Alternatively, delete files manually as needed.

### 4. Stage and Commit the Changes

```sh
git add -A
```

### 5. Push to GitHub

```sh
git push origin main
```

---

**Note:**  
Deleting files does not erase commit history. You can restore previous files by reverting to an earlier commit if needed.
