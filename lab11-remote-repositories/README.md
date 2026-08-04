# Lab 11 - Remote Repositories

## Objective

Learn how to connect a local Git repository to a remote repository and synchronize changes between them.

---

## Prerequisites

- GitHub account
- Existing local Git repository

---

## Lab Setup

Verify existing remotes.

```bash
git remote -v
```

If no remote exists, create a new repository on GitHub.

---

## Steps

### Add a Remote Repository

```bash
git remote add origin https://github.com/<username>/git-labs.git
```

Verify.

```bash
git remote -v
```

---

### Rename a Remote

```bash
git remote rename origin github
```

---

### Remove a Remote

```bash
git remote remove github
```

---

### Push to Remote

```bash
git push -u origin main
```

The `-u` flag sets the upstream branch, allowing future pushes with simply:

```bash
git push
```

---

### Clone a Repository

```bash
git clone https://github.com/<username>/git-labs.git
```

---

## Verification

```bash
git remote -v
git branch -vv
```

---

## Production Use Case

Remote repositories enable collaboration between developers, CI/CD systems, and deployment pipelines by providing a shared source of truth.

---

## Common Mistakes

- Adding the wrong remote URL.
- Forgetting to configure the upstream branch.
- Accidentally pushing to the wrong branch.

---

## Interview Questions

### What is a remote repository?

A remote repository is a shared Git repository hosted on platforms like GitHub, GitLab, or Bitbucket.

---

### What does `git push -u origin main` do?

It pushes the local `main` branch to the remote and sets it as the upstream branch for future pushes and pulls.

---

## Key Takeaways

- Remote repositories enable collaboration.
- Always verify remotes using `git remote -v`.
- Configure upstream branches for easier workflows.
