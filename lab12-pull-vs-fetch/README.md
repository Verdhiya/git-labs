# Lab 12 - Git Pull vs Git Fetch

## Objective

Understand the difference between `git fetch` and `git pull` and when to use each command.

---

## Prerequisites

- Completed Remote Repository lab

---

## Lab Setup

Check the current branch.

```bash
git branch
```

View remote branches.

```bash
git branch -r
```

---

## Steps

### Fetch Remote Changes

```bash
git fetch
```

Inspect the fetched changes.

```bash
git log --oneline --graph --all
```

Notice that your working branch is unchanged.

---

### Pull Remote Changes

```bash
git pull
```

Git performs:

```text
git fetch
+
git merge
```

(or rebase if configured).

---

### Fetch a Specific Remote

```bash
git fetch origin
```

---

### Pull a Specific Branch

```bash
git pull origin main
```

---

## Verification

```bash
git status
git log --graph --oneline --all
```

---

## Production Use Case

Many teams prefer using `git fetch` before reviewing incoming changes. This allows developers to inspect updates before merging them into their working branch.

---

## Common Mistakes

- Assuming `git fetch` updates the working directory.
- Running `git pull` without reviewing incoming changes.
- Forgetting that `git pull` may create merge commits.

---

## Interview Questions

### Difference between Fetch and Pull?

`git fetch` downloads remote changes without modifying the current branch.

`git pull` downloads and integrates remote changes into the current branch.

---

### Which is safer?

`git fetch` is generally safer because it allows you to review changes before merging them.

---

## Key Takeaways

- Fetch downloads only.
- Pull downloads and integrates.
- Fetch is preferred when reviewing remote changes.
