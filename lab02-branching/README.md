# Lab 02 - Branching

## Objective

Learn how to create, switch, rename, list, and delete branches while understanding how Git manages branch pointers.

---

## Prerequisites

- Completed Lab 01

---

## Lab Setup

```bash
git branch
```

---

## Steps

### Create a Branch

```bash
git branch feature/login
```

List branches.

```bash
git branch
```

---

### Switch Branch

```bash
git switch feature/login
```

Verify:

```bash
git branch
```

---

### Create and Switch

```bash
git switch -c feature/dashboard
```

---

### Rename Branch

```bash
git branch -m feature/ui
```

---

### Delete Branch

```bash
git switch main
git branch -d feature/ui
```

Force delete:

```bash
git branch -D feature/ui
```

---

## Verification

```bash
git branch
git log --oneline --graph --all
```

---

## Production Use Case

Feature branches isolate development work, allowing teams to develop, test, and review changes independently before merging into the main branch.

---

## Common Mistakes

- Working directly on `main`.
- Deleting branches that contain unmerged work.
- Forgetting to switch branches before making changes.

---

## Interview Questions

### What is a Git branch?

A lightweight pointer to a commit that enables parallel development.

---

### Why are branches lightweight?

A branch stores only a reference to the latest commit rather than copying the repository.

---

## Key Takeaways

- Branches are pointers.
- Creating branches is inexpensive.
- Feature branches support isolated development.
