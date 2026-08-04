# Git Labs

A hands-on Git learning repository focused on real-world workflows, production scenarios, and DevOps interview preparation.

Instead of only explaining Git commands, each lab demonstrates how Git behaves internally, why a workflow is used, and where it is applied in production environments.

---

## Objectives

- Understand Git fundamentals beyond memorizing commands.
- Learn how Git manages history, branches, and commits.
- Practice common production workflows.
- Build confidence for DevOps and SRE interviews.
- Create reproducible labs for future reference.

---

## Repository Structure

```text
git-labs/
├── lab01-initialize-repository
├── lab02-branching
├── lab03-merge
├── lab04-merge-conflict
├── lab05-rebase
├── lab06-stash
├── lab07-reset
├── lab08-cherry-pick
├── lab09-revert
├── lab10-tags
├── lab11-remote-repositories
├── lab12-pull-vs-fetch
├── lab13-reflog
├── notes
└── README.md
```

---

# Labs

| Lab | Topic | Description |
|------|-------|-------------|
| Lab 01 | Initialize Repository | Repository initialization, staging area, commits, and Git fundamentals. |
| Lab 02 | Branching | Creating, switching, deleting, and managing branches. |
| Lab 03 | Merge | Fast-forward and three-way merge workflows. |
| Lab 04 | Merge Conflict | Simulating and resolving merge conflicts. |
| Lab 05 | Rebase | Rebasing branches, history rewriting, and clean commit history. |
| Lab 06 | Git Stash | Saving work in progress and restoring changes. |
| Lab 07 | Git Reset | Soft, mixed, and hard reset with practical use cases. |
| Lab 08 | Cherry-pick | Backporting commits and selective commit replay. |
| Lab 09 | Revert | Safely undoing changes while preserving history. |
| Lab 10 | Tags | Lightweight and annotated tags for releases. |
| Lab 11 | Remote Repositories | Working with GitHub remotes, push, pull, clone, and fetch. |
| Lab 12 | Pull vs Fetch | Understanding synchronization with remote repositories. |
| Lab 13 | Reflog | Recovering lost commits and navigating Git history. |

---

# Skills Covered

- Repository initialization
- Git object model
- Branch management
- Merge strategies
- Merge conflict resolution
- Interactive rebase
- Commit history management
- Cherry-pick workflows
- History recovery using Reflog
- Safe rollback strategies
- Release tagging
- Remote collaboration
- Production Git workflows

---

# Production Scenarios Covered

This repository includes practical workflows commonly used in production environments:

- Feature branch development
- Pull request workflows
- Hotfix releases
- Release branch management
- Cherry-picking critical fixes
- Recovering lost commits
- Safe rollback using Git Revert
- Team collaboration with remote repositories
- Release version tagging

---

# Interview Topics

This repository helps prepare for common DevOps interview questions such as:

- Difference between Merge and Rebase
- Reset vs Revert
- Pull vs Fetch
- Fast-forward vs Three-way Merge
- Cherry-pick use cases
- Git Reflog recovery
- Merge conflict resolution
- Branching strategies
- Git internals
- Git object database

---

# Prerequisites

- Git 2.x or later
- Linux, macOS, or Windows
- Basic command-line knowledge

---

# How to Use

Clone the repository:

```bash
git clone <repository-url>
```

Move into the repository:

```bash
cd git-labs
```

Open any lab directory and follow the steps to reproduce the exercises.

Each lab is independent and can be completed separately.

---

# Target Audience

- DevOps Engineers
- Site Reliability Engineers (SRE)
- Platform Engineers
- Cloud Engineers
- System Administrators
- Students preparing for Git interviews

---

# Future Improvements

- Architecture diagrams
- Git commit graph visualizations
- Production troubleshooting scenarios
- GitHub workflow examples
- Interactive exercises
- Common interview mistakes
- Additional advanced Git labs

---

# License

This project is intended for educational purposes.
