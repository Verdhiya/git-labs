# Git Interview Notes

## Git Architecture

- Working Directory
- Staging Area (Index)
- Local Repository
- Remote Repository

---

## Git Workflow

Working Directory
        ↓
git add
        ↓
Staging Area
        ↓
git commit
        ↓
Local Repository
        ↓
git push
        ↓
Remote Repository

---

## Branch Commands

git branch

git switch

git checkout

git merge

git rebase

---

## Merge vs Rebase

| Merge | Rebase |
|--------|--------|
| Preserves history | Rewrites history |
| Creates merge commit | Linear history |
| Safe on shared branches | Avoid on shared branches |

---

## Reset

Soft

Mixed

Hard

When to use each.

---

## Revert

Creates inverse commit.

Safe after push.

---

## Cherry-pick

Copies selected commits.

Creates new SHA.

Hotfix backport.

---

## Stash

Save work.

Restore later.

apply vs pop.

---

## Reflog

Recover lost commits.

Recover after reset.

Recover after rebase.

---

## Tags

Lightweight

Annotated

Release versions

---

## Pull vs Fetch

Fetch

↓

Downloads

Pull

↓

Fetch + Merge

---

## Most Asked Interview Questions

Difference between:

- Merge vs Rebase
- Reset vs Revert
- Pull vs Fetch
- Clone vs Fork
- Tags
- HEAD
- Detached HEAD
- Cherry-pick
- Reflog

---

## Production Best Practices

✔ Feature branches

✔ Small commits

✔ Meaningful commit messages

✔ Pull Requests

✔ Protected main branch

✔ Rebase local branches

✔ Revert instead of reset after push

✔ Use tags for releases

✔ Cherry-pick for hotfixes

---

## Common Mistakes

- Force push to main
- Hard reset after push
- Large commits
- Working on main
- Forgetting to pull before push

---

## 10-Minute Interview Revision

- Git Architecture
- Branches
- Merge
- Rebase
- Merge Conflict
- Stash
- Reset
- Revert
- Cherry-pick
- Tags
- Remote
- Fetch vs Pull
- Reflog
