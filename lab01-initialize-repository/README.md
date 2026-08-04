# Lab 01 - Initialize Repository

## Objective

Learn how to initialize a Git repository, understand the repository structure, stage files, create commits, and inspect repository status.

---

## Prerequisites

- Git installed
- Linux terminal
- Basic command-line knowledge

---

## Lab Setup

Create a new directory and initialize a Git repository.

```bash
mkdir lab01-initialize-repository
cd lab01-initialize-repository

git init
```

Verify the repository.

```bash
git status
```

---

## Steps

### Step 1 - Create a File

```bash
echo "# Git Lab" > README.md
```

---

### Step 2 - Check Repository Status

```bash
git status
```

Observe that the file is untracked.

---

### Step 3 - Stage the File

```bash
git add README.md
```

Verify:

```bash
git status
```

---

### Step 4 - Commit the Changes

```bash
git commit -m "Initial commit"
```

Verify:

```bash
git log --oneline
```

---

## Verification

```bash
git status
git log --oneline
```

Expected:

- Working tree clean
- Initial commit visible

---

## Production Use Case

Every software project begins with repository initialization. Commits provide a reliable history of changes and enable collaboration across development teams.

---

## Common Mistakes

- Forgetting to stage files before committing.
- Creating meaningless commit messages.
- Committing generated or temporary files.

---

## Interview Questions

### What does `git init` do?

Creates a new Git repository by initializing the `.git` directory that stores repository metadata and history.

---

### Difference between tracked and untracked files?

Tracked files are managed by Git. Untracked files exist in the working directory but are not yet part of version control.

---

## Key Takeaways

- Initialize repositories with `git init`.
- Stage changes using `git add`.
- Create commits using `git commit`.
- Use `git status` to inspect repository state.
