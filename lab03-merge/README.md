# Lab 03 - Merge

## Objective

Understand how Git combines changes from different branches using fast-forward and three-way merge strategies.

---

## Prerequisites

- Completed Lab 02

---

## Lab Setup

Create a feature branch.

```bash
git switch -c feature/login
```

Make a commit.

```bash
echo "Login feature" >> app.txt

git add app.txt
git commit -m "Add login feature"
```

Return to main.

```bash
git switch main
```

---

## Steps

### Fast-Forward Merge

```bash
git merge feature/login
```

Visualize history.

```bash
git log --oneline --graph --all
```

---

### Three-Way Merge

Create two branches with different commits.

Merge them.

Observe the merge commit.

---

## Verification

```bash
git log --graph --oneline --all
```

---

## Production Use Case

Merging integrates completed feature branches into shared branches such as `main` or `release`. It is the most common workflow used in collaborative software development.

---

## Common Mistakes

- Merging without reviewing changes.
- Ignoring merge conflicts.
- Creating unnecessary merge commits.

---

## Interview Questions

### What is a fast-forward merge?

Occurs when the target branch has no additional commits and Git simply moves the branch pointer forward.

---

### What is a three-way merge?

A merge that combines changes from two diverged branches using their common ancestor and creates a merge commit.

---

### Merge vs Rebase?

Merge preserves branch history by creating a merge commit. Rebase rewrites commit history to produce a linear history.

---

## Key Takeaways

- Git supports fast-forward and three-way merges.
- Merge preserves branch history.
- Merge conflicts occur when changes overlap.
