# Lab 06 - Git Stash

## Objective

Learn how to temporarily save uncommitted changes and restore them later without creating unnecessary commits.

---

## Prerequisites

- Completed Lab 05

---

## Lab Setup

Modify a file.

```bash
echo "Temporary work" >> app.txt
```

Check status.

```bash
git status
```

---

## Steps

### Save Changes

```bash
git stash
```

Verify.

```bash
git status
```

---

### View Stashes

```bash
git stash list
```

---

### Restore Changes

```bash
git stash apply
```

---

### Apply and Remove

```bash
git stash pop
```

---

### Remove a Stash

```bash
git stash drop
```

Remove all stashes.

```bash
git stash clear
```

---

## Verification

```bash
git stash list
git status
```

---

## Production Use Case

Stash is useful when an urgent production issue requires switching branches before your current work is ready to commit.

---

## Common Mistakes

- Forgetting stashed work.
- Using stash instead of proper commits for long-term work.
- Clearing stashes accidentally.

---

## Interview Questions

### What is Git Stash?

A mechanism for temporarily saving uncommitted changes while returning the working directory to a clean state.

---

### Difference between apply and pop?

`apply` restores the stash while keeping it in the stash list.

`pop` restores the stash and removes it from the stash list.

---

## Key Takeaways

- Stash temporarily saves work.
- Useful for context switching.
- Prefer commits for long-term work.
