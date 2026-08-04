# Lab 04 - Merge Conflict

## Objective

Learn how merge conflicts occur, how Git identifies conflicting changes, and how to resolve them safely.

---

## Prerequisites

- Completed Lab 03

---

## Lab Setup

Create a new feature branch.

```bash
git switch -c feature/login
```

Create a file.

```bash
echo "Version from feature branch" > app.txt
git add app.txt
git commit -m "Feature branch update"
```

Switch back to main.

```bash
git switch main
```

Modify the same line.

```bash
echo "Version from main branch" > app.txt
git add app.txt
git commit -m "Main branch update"
```

---

## Steps

### Merge the Feature Branch

```bash
git merge feature/login
```

Git reports a merge conflict.

---

### View Conflict

Open the file.

```text
<<<<<<< HEAD
Version from main branch
=======
Version from feature branch
>>>>>>> feature/login
```

---

### Resolve Conflict

Edit the file manually.

Example:

```text
Version from main branch
Version from feature branch
```

Stage the resolved file.

```bash
git add app.txt
```

Complete the merge.

```bash
git commit
```

---

## Verification

```bash
git status
git log --graph --oneline --all
```

---

## Production Use Case

Merge conflicts commonly occur when multiple developers modify the same file or nearby lines. Resolving conflicts correctly prevents accidental loss of code.

---

## Common Mistakes

- Deleting conflict markers incorrectly.
- Forgetting to stage resolved files.
- Choosing the wrong version during resolution.
- Blindly accepting changes without reviewing them.

---

## Interview Questions

### Why do merge conflicts occur?

Git cannot automatically determine which change should be kept when the same section of code has been modified differently.

---

### How do you resolve a merge conflict?

Review the conflicting changes, edit the file, remove conflict markers, stage the file, and complete the merge commit.

---

## Key Takeaways

- Merge conflicts are normal.
- Git pauses the merge until conflicts are resolved.
- Always review conflicting changes before committing.
