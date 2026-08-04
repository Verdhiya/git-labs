# Lab 05 - Rebase

## Objective

Learn how Git rebase moves commits onto another branch to create a cleaner, linear commit history.

---

## Prerequisites

- Completed Lab 03

---

## Lab Setup

Create a feature branch.

```bash
git switch -c feature/api
```

Make a commit.

```bash
echo "API Feature" >> app.txt
git add app.txt
git commit -m "Add API feature"
```

Return to main.

```bash
git switch main
```

Make another commit.

```bash
echo "Main branch update" >> app.txt
git add app.txt
git commit -m "Main update"
```

---

## Steps

Switch back.

```bash
git switch feature/api
```

Rebase onto main.

```bash
git rebase main
```

Visualize history.

```bash
git log --graph --oneline --all
```

---

### Handling Rebase Conflicts

Resolve the conflict.

Stage the file.

```bash
git add app.txt
```

Continue.

```bash
git rebase --continue
```

Abort if required.

```bash
git rebase --abort
```

---

## Verification

```bash
git log --graph --oneline --all
```

---

## Production Use Case

Rebase is commonly used before opening a pull request to keep feature branches up to date with the latest changes while maintaining a clean commit history.

---

## Common Mistakes

- Rebasing shared branches.
- Force pushing without understanding the impact.
- Ignoring conflicts during rebase.

---

## Interview Questions

### Merge vs Rebase?

Merge preserves history by creating a merge commit.

Rebase rewrites commit history to produce a linear history.

---

### When should rebase be avoided?

Avoid rebasing commits that have already been pushed and shared with other developers.

---

## Key Takeaways

- Rebase creates a linear history.
- Rebase rewrites commit history.
- Do not rebase shared branches.
