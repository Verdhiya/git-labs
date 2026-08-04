# Lab 13 - Git Reflog

## Objective

Learn how Git Reflog tracks reference updates and helps recover lost commits after operations such as reset, rebase, or branch deletion.

---

## Prerequisites

- Completed Git Reset lab

---

## Lab Setup

Create a commit.

```bash
echo "Recovery Test" >> app.txt
git add app.txt
git commit -m "Recovery commit"
```

View history.

```bash
git log --oneline
```

---

## Steps

### View Reflog

```bash
git reflog
```

Observe previous HEAD positions.

---

### Recover a Lost Commit

Identify the desired commit from the reflog.

Reset to it.

```bash
git reset --hard HEAD@{2}
```

Alternatively:

```bash
git reset --hard <commit-hash>
```

---

### Inspect Commit

```bash
git log --oneline
```

---

## Verification

```bash
git reflog
git log --oneline
```

---

## Production Use Case

Reflog is invaluable for recovering work after accidental resets, rebases, or deleted branches before Git garbage collection removes unreachable commits.

---

## Common Mistakes

- Assuming deleted commits are permanently lost.
- Waiting too long before recovery.
- Confusing `git log` with `git reflog`.

---

## Interview Questions

### What is Git Reflog?

Reflog records updates to Git references such as HEAD, allowing developers to recover commits that are no longer visible in the branch history.

---

### Can Reflog recover a hard reset?

Yes. As long as the commit still exists in the reflog and has not been garbage collected, it can be recovered.

---

## Key Takeaways

- Reflog tracks reference history.
- Useful for recovering lost commits.
- One of Git's most valuable recovery tools.
