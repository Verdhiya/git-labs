# Lab 09 - Git Revert

## Objective

Learn how to safely undo changes while preserving Git history.

---

## Prerequisites

- Completed Git Reset lab

---

## Lab Setup

Create a commit.

```bash
echo "Temporary Change" >> app.txt
git add app.txt
git commit -m "Temporary update"
```

View history.

```bash
git log --oneline
```

---

## Steps

### Revert a Commit

```bash
git revert <commit-hash>
```

Git creates a new commit that reverses the selected commit.

---

### Verify

```bash
git log --oneline
```

Observe the newly created revert commit.

---

## Verification

```bash
git log --graph --oneline
git status
```

---

## Production Use Case

Revert is the preferred method for undoing commits that have already been pushed to shared repositories.

---

## Common Mistakes

- Using Reset instead of Revert on shared branches.
- Reverting the wrong commit.
- Forgetting that Revert creates a new commit.

---

## Interview Questions

### Reset vs Revert?

Reset rewrites history.

Revert preserves history by creating a new commit that reverses previous changes.

---

### Why is Revert safer in production?

Because it maintains a complete and auditable commit history without requiring force pushes.

---

## Key Takeaways

- Revert preserves history.
- Safe for shared branches.
- Creates a new commit.
