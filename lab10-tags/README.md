# Lab 10 - Git Tags

## Objective

Learn how to create, manage, and use Git tags for marking releases and important milestones.

---

## Prerequisites

- Completed previous labs

---

## Lab Setup

View commit history.

```bash
git log --oneline
```

---

## Steps

### Create a Lightweight Tag

```bash
git tag v1.0
```

---

### Create an Annotated Tag

```bash
git tag -a v1.1 -m "Release version 1.1"
```

---

### List Tags

```bash
git tag
```

---

### View Tag Details

```bash
git show v1.1
```

---

### Push Tags

```bash
git push origin --tags
```

---

## Verification

```bash
git tag
```

---

## Production Use Case

Tags are used to identify release versions, rollback points, and deployment milestones.

---

## Common Mistakes

- Forgetting to push tags.
- Confusing branches with tags.

---

## Interview Questions

### Lightweight vs Annotated Tags?

Lightweight tags are simple references.

Annotated tags store metadata such as author, date, and message.

---

## Key Takeaways

- Tags mark releases.
- Tags are immutable references.
- Push tags separately.
