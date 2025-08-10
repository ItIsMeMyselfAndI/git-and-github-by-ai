# 5. Collaborating with Remotes: Pushing, Pulling, and Syncing

Git’s true power shines when working with others. Remotes (like GitHub) let you share your work and stay up to date with your team or the broader developer community.

---

## 5.1 What is a Remote?

A **remote** is a version of your repository hosted elsewhere (usually on GitHub).  
The default remote is usually named `origin`.

---

## 5.2 Pushing Your Work to GitHub

**Push** uploads your local commits to a remote repository.

```bash
git push origin main
```
- `origin` is the remote name.
- `main` is the branch name.

### First-time push for a new branch:
```bash
git push -u origin feature-xyz
```
- `-u` sets up tracking, so future `git push`/`git pull` commands know which remote/branch to use by default.

---

## 5.3 Pulling and Fetching

**Pull** downloads new commits from the remote and merges them into your current branch.

```bash
git pull origin main
```

**Fetch** downloads new commits from the remote, but doesn’t merge:

```bash
git fetch origin
```
- After `git fetch`, view new changes with `git log origin/main`.
- To merge fetched changes: `git merge origin/main`.

---

## 5.4 Working with Multiple Collaborators

1. **Sync regularly:**  
   Always pull before you start working and before you push, to minimize conflicts.

2. **Resolve conflicts:**  
   If two people edit the same part of a file, you’ll get a conflict. Git will mark the file and you’ll need to choose what to keep (see previous section for resolving merge conflicts).

3. **Stay on branches:**  
   Make changes on feature branches, not directly on `main`, to keep the main branch stable.

---

## 5.5 Forks and Upstream Remotes

When contributing to open source, you usually **fork** a repo (copy it to your account) and then clone your fork.

To keep up to date with the original repo:

```bash
git remote add upstream git@github.com:original-owner/repo.git
git fetch upstream
git merge upstream/main
# or, to rebase:
git rebase upstream/main
```

- `origin` = your fork
- `upstream` = the original repo

---

## 5.6 Summary Table

| Command                                | Purpose                                         |
|-----------------------------------------|-------------------------------------------------|
| `git push origin <branch>`              | Push your branch to the remote repository       |
| `git pull origin <branch>`              | Pull changes from remote and merge              |
| `git fetch origin`                      | Fetch changes from remote, don’t merge          |
| `git remote add upstream <url>`         | Add a second remote (for forks)                 |
| `git merge upstream/main`               | Merge upstream changes into your branch         |
| `git rebase upstream/main`              | Rebase your branch on top of upstream changes   |

---

**You’re now ready to collaborate with others using remotes!**

---

Next: [How to use Pull Requests (PRs) and code review on GitHub—the professional way to propose, discuss, and merge changes.](./06-pull-requests-and-code-review.md)
