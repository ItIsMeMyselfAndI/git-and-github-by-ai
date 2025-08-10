# 4. Branching and Merging

Branching is a powerful feature in Git that lets you work on new features, bug fixes, or experiments in isolation from the main codebase. Once your work is ready, you can merge it back into the main branch.

---

## 4.1 What is a Branch?

A **branch** is a parallel version of your project. The default branch is usually called `main` (sometimes `master`). Developers create branches to:
- Work on features independently
- Fix bugs without affecting the main code
- Experiment safely

---

## 4.2 Creating and Switching Branches

### Create a new branch:
```bash
git branch feature-xyz
```
This creates a branch called `feature-xyz` but does NOT switch to it.

### Switch to a branch:
```bash
git checkout feature-xyz
```
or (modern syntax, preferred):
```bash
git switch feature-xyz
```

### Create and switch in one command:
```bash
git checkout -b feature-xyz
```
or:
```bash
git switch -c feature-xyz
```

---

## 4.3 Making Changes on a Branch

1. Edit files as needed.
2. Stage and commit your changes:
   ```bash
   git add .
   git commit -m "Describe your changes"
   ```
3. Check which branch you’re on:
   ```bash
   git branch
   ```
   - The current branch is marked with `*`.

---

## 4.4 Merging Branches

Once your work is complete, merge your feature branch into `main`.

1. Switch to the `main` branch:
   ```bash
   git checkout main
   ```
   or:
   ```bash
   git switch main
   ```

2. Bring your feature branch changes into `main`:
   ```bash
   git merge feature-xyz
   ```
   - This combines the histories.
   - If there are no conflicts, Git creates a new merge commit.

---

## 4.5 Deleting a Branch

After a successful merge, you can delete your feature branch:

```bash
git branch -d feature-xyz
```
- The `-d` flag prevents deletion if the branch isn’t fully merged.

---

## 4.6 Resolving Merge Conflicts

Sometimes, changes in different branches overlap and Git can’t merge automatically. You’ll see a conflict message.

**To resolve:**
1. Open the conflicted files and look for conflict markers:
   ```
   <<<<<<< HEAD
   (your changes)
   =======
   (other branch's changes)
   >>>>>>> feature-xyz
   ```
2. Edit the file to keep what you want.
3. After resolving, add and commit:
   ```bash
   git add conflicted-file
   git commit -m "Resolve merge conflict"
   ```

---

## 4.7 Summary Table

| Command                                | Purpose                                 |
|-----------------------------------------|-----------------------------------------|
| `git branch <name>`                     | Create a new branch                     |
| `git switch <name>` / `git checkout <name>` | Switch to a branch                    |
| `git switch -c <name>` / `git checkout -b <name>` | Create and switch to a new branch |
| `git merge <branch>`                    | Merge branch into current branch        |
| `git branch -d <name>`                  | Delete a branch                         |

---

Next: [Collaborating with others using remotes—pushing, pulling, and syncing your work with GitHub!](./05-collaborating-with-remotes.md)
