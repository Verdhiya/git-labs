# Lab 08 - Git Cherry-pick

## Objective

Learn how to apply specific commits from one branch to another without merging the entire branch.

---

## Prerequisites

- Completed Merge and Branching labs

---

## Lab Setup

Create a feature branch.

```bash
git switch -c feature/hotfix
```

Make a commit.

```bash
echo "Critical Bug Fix" >> app.txt
git add app.txt
git commit -m "Fix critical bug"
```

Copy the commit hash.

```bash
git log --oneline
```

Return to main.

```bash
git switch main
```

---

## Steps

### Cherry-pick a Commit

```bash
git cherry-pick <commit-hash>
```

Verify.

```bash
git log --oneline
```

---

### Cherry-pick Multiple Commits

```bash
git cherry-pick commit1 commit2
```

---

### Cherry-pick a Range

```bash
git cherry-pick C^..F
```

---

### Cherry-pick with Traceability

```bash
git cherry-pick -x <commit>
```

Adds the original commit hash to the commit message.

---

### Conflict Handling

Continue:

```bash
git cherry-pick --continue
```

Skip:

```bash
git cherry-pick --skip
```

Abort:

```bash
git cherry-pick --abort
```

---

## Verification

```bash
git log --graph --oneline --all
```

---

## Production Use Case

Cherry-pick is commonly used to backport critical bug fixes into release branches without merging unfinished features.

---

## Common Mistakes

- Cherry-picking dependent commits without required changes.
- Forgetting to resolve conflicts.
- Assuming the original commit SHA is preserved.

---

## Interview Questions

### Why does Cherry-pick create a new commit?

Because Git replays the patch and creates a new commit object with a different parent, resulting in a new SHA.

---

### Merge vs Cherry-pick?

Merge integrates entire branch history.

Cherry-pick applies selected commits only.

---

## Key Takeaways

- Cherry-pick replays commits.
- New commit means new SHA.
- Commonly used for production hotfixes.
