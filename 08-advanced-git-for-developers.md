# 8. Advanced Git for Developers

Now that you’re comfortable with everyday Git workflows, let’s explore advanced features that help you manage complex changes, debug issues, and keep your history clean.

---

## 8.1 Stashing Changes

Stash saves your uncommitted changes for later, letting you switch branches or pull updates without losing work.

- **Save your changes:**
  ```bash
  git stash
  ```
- **List stashes:**
  ```bash
  git stash list
  ```
- **Apply the latest stash:**
  ```bash
  git stash apply
  ```
- **Apply and remove the stash:**
  ```bash
  git stash pop
  ```

---

## 8.2 Cherry-Picking Commits

Cherry-picking lets you apply a specific commit from one branch onto another.

- **Find the commit hash** you want to cherry-pick (use `git log`).
- **Apply it to your current branch:**
  ```bash
  git cherry-pick <commit-hash>
  ```

---

## 8.3 Interactive Rebase

Interactive rebase helps you rewrite, squash, or reorder commits for a cleaner history.

- **Start an interactive rebase for the last 3 commits:**
  ```bash
  git rebase -i HEAD~3
  ```
- In the editor, use commands like `pick`, `squash`, or `edit` for each commit.
- Save and close the editor to continue.

**Common use cases:**
- Squash multiple commits into one before merging a feature branch.
- Edit old commit messages.

---

## 8.4 Bisect: Finding Bugs Efficiently

`git bisect` helps you find which commit introduced a bug.

- **Start bisect:**
  ```bash
  git bisect start
  ```
- **Mark a bad commit** (where the bug is present):
  ```bash
  git bisect bad
  ```
- **Mark a good commit** (where the bug didn’t exist):
  ```bash
  git bisect good <commit-hash>
  ```
- Git will automatically check out commits between good and bad. Test each and mark as `good` or `bad` until the culprit is found.

- **End bisect:**
  ```bash
  git bisect reset
  ```

---

## 8.5 Undoing Changes

- **Undo changes in a file (restore from last commit):**
  ```bash
  git checkout -- <file>
  ```
  Or, modern Git:
  ```bash
  git restore <file>
  ```
- **Undo the latest commit (keep changes):**
  ```bash
  git reset --soft HEAD~1
  ```
- **Undo the latest commit (discard changes):**
  ```bash
  git reset --hard HEAD~1
  ```
- **Revert a commit (creates a new commit that undoes changes):**
  ```bash
  git revert <commit-hash>
  ```

---

## 8.6 Working with Submodules

Submodules let you include other Git repositories inside your repo (useful for dependencies).

- **Add a submodule:**
  ```bash
  git submodule add <repo-url> path/to/submodule
  ```
- **Clone a repo with submodules:**
  ```bash
  git clone --recurse-submodules <repo-url>
  ```
- **Update submodules:**
  ```bash
  git submodule update --init --recursive
  ```

---

## 8.7 Sparse Checkout and Partial Clone

For large repos, you can check out only part of the project.

- **Enable sparse checkout:**
  ```bash
  git sparse-checkout init --cone
  git sparse-checkout set path/to/folder
  ```
- **Partial clone (download only what you need):**
  ```bash
  git clone --filter=blob:none <repo-url>
  ```

---

## 8.8 Summary Table

| Feature                | Command/Usage                            |
|------------------------|------------------------------------------|
| Stash changes          | `git stash`, `git stash pop`             |
| Cherry-pick commit     | `git cherry-pick <commit-hash>`          |
| Interactive rebase     | `git rebase -i HEAD~N`                   |
| Bisect                 | `git bisect start`, `good`, `bad`        |
| Undo changes           | `git reset`, `git revert`, `git restore` |
| Submodules             | `git submodule add` etc.                 |
| Sparse checkout        | `git sparse-checkout`                    |

---

Next: [Advanced GitHub usage—automation with Actions, managing secrets, GitHub Packages, Pages, and more!](./09-advanced-github-usage.md)
