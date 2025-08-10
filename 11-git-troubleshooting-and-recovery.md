# 11. Git Troubleshooting and Recovery

Even experienced developers make mistakes with Git! The good news: most mistakes can be fixed. Here’s how to recover lost work, undo errors, and handle common pitfalls.

---

## 11.1 Undoing Local Changes

- **Discard changes in a file (unstaged):**
  ```bash
  git checkout -- <file>
  ```
  Or, in modern Git:
  ```bash
  git restore <file>
  ```
- **Unstage a file (keep your edits, just remove from the staging area):**
  ```bash
  git reset HEAD <file>
  ```
- **Discard ALL local changes (dangerous!):**
  ```bash
  git reset --hard
  ```

---

## 11.2 Amending the Most Recent Commit

- **Edit the last commit message or add forgotten files:**
  ```bash
  git commit --amend
  ```
  This opens your editor to update the commit message and/or includes any staged changes.

---

## 11.3 Recovering Deleted Files

- **If you accidentally deleted a tracked file:**
  ```bash
  git checkout HEAD -- <file>
  ```
  Or:
  ```bash
  git restore --source=HEAD <file>
  ```

---

## 11.4 Restoring a Previous Commit

- **Move HEAD and branch pointer back (rewrites history!):**
  ```bash
  git reset --hard <commit-hash>
  ```
- **Create a new commit that undoes a previous one (safe for shared branches):**
  ```bash
  git revert <commit-hash>
  ```

---

## 11.5 Recovering Lost Commits

- **Find “lost” commits (e.g., after a reset or rebase):**
  ```bash
  git reflog
  ```
  This shows a log of all HEAD changes. Use a commit hash from the reflog to restore it:
  ```bash
  git checkout <hash>
  ```

---

## 11.6 Fixing a Broken Merge

- **Abort a merge in progress:**
  ```bash
  git merge --abort
  ```
- **Abort a rebase in progress:**
  ```bash
  git rebase --abort
  ```

---

## 11.7 Resolving Merge Conflicts (Recap)

1. Open conflicted files and look for `<<<<<<<`, `=======`, `>>>>>>>` markers.
2. Edit to keep the correct changes.
3. Stage and commit the file:
   ```bash
   git add <file>
   git commit
   ```

---

## 11.8 Common Errors and Solutions

| Error Message                               | What It Means & How to Fix                                   |
|---------------------------------------------|--------------------------------------------------------------|
| `fatal: Not a git repository`               | Run commands inside a git-initialized directory.             |
| `error: failed to push refs`                | Sync with remote (`git pull --rebase`) before pushing.       |
| `Merge conflict in <file>`                  | Manually resolve conflicts, then commit.                     |
| `detached HEAD`                             | You’re not on a branch; switch back with `git switch <branch>`|
| `Permission denied (publickey)`             | SSH key isn’t set up; check your SSH keys and GitHub config. |
| `rejected - non-fast-forward`               | Someone pushed to remote; pull and resolve before pushing.   |

---

## 11.9 Good Habits to Avoid Trouble

- Commit and push often.
- Pull before you start working.
- Never use `--force` unless you really know what you’re doing!
- Always review the commands before running anything destructive (`reset --hard`, `clean`, etc.).
- Use branches for features, fixes, and experiments.

---

## 11.10 When All Else Fails

- Ask for help! Provide error messages and what you did before the problem.
- The [GitHub Community](https://github.com/community), Stack Overflow, and project maintainers are great resources.

---

## 11.11 Summary Table

| Problem               | Solution                                  |
|-----------------------|-------------------------------------------|
| Undo file changes     | `git restore <file>`                      |
| Unstage changes       | `git reset HEAD <file>`                   |
| Amend last commit     | `git commit --amend`                      |
| Recover deleted file  | `git restore --source=HEAD <file>`        |
| Find lost commits     | `git reflog`                              |
| Abort merge/rebase    | `git merge --abort` / `git rebase --abort`|

---

**Congratulations!**  
You’ve completed the practical Git & GitHub guide for developers. You’re ready to collaborate, contribute, and troubleshoot with confidence.

**Next:** (Optional) Popular Git GUI tools, resources, and further learning!