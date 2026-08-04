# Lab 07 - Git Reset

## Objective

Learn how Git Reset modifies the current branch and understand the differences between `--soft`, `--mixed`, and `--hard`.

---

## Prerequisites

- Completed previous labs
- At least two commits in the repository

---

## Lab Setup

Create a test file and commit it.

```bash
echo "Version 1" > app.txt
git add app.txt
git commit -m "Add app.txt"

echo "Version 2" >> app.txt
git add app.txt
git commit -m "Update app.txt"
```

View commit history.

```bash
git log --oneline
```

---

## Steps

### Soft Reset

```bash
git reset --soft HEAD~1
```

Verify:

```bash
git status
```

Changes remain staged.

---

### Mixed Reset (Default)

```bash
git reset HEAD~1
```

or

```bash
git reset --mixed HEAD~1
```

Changes remain in the working directory but are unstaged.

---

### Hard Reset

```bash
git reset --hard HEAD~1
```

Verify:

```bash
git status
git log --oneline
```

The commit and working directory changes are removed.

---

## Verification

```bash
git log --oneline
git status
```

---

## Production Use Case

Reset is useful for cleaning up local commits before they are pushed. Avoid using `--hard` on shared branches.

---

## Common Mistakes

- Using `--hard` without understanding data loss.
- Resetting commits that have already been pushed.
- Confusing Reset with Revert.

---

## Interview Questions

### Difference between Soft, Mixed, and Hard Reset?

- **Soft:** Moves HEAD, keeps changes staged.
- **Mixed:** Moves HEAD, unstages changes.
- **Hard:** Moves HEAD and discards working directory changes.

---

### When should Reset be avoided?

Avoid resetting commits that have already been shared with others.

---

## Key Takeaways

- Reset rewrites history.
- Hard reset permanently discards local changes.
- Safe before pushing; risky after pushing.
