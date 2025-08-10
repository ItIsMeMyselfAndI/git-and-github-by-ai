# 6. Pull Requests and Code Review on GitHub

Pull Requests (PRs) are the professional way to propose, discuss, and merge changes on GitHub. They enable code review, collaboration, and ensure only high-quality code enters important branches like `main`.

---

## 6.1 What is a Pull Request?

A **Pull Request** is a request to merge changes from one branch (usually a feature or fix branch) into another (often `main` or `dev`). It’s also the place for discussion, review, and approval of your work before merging.

---

## 6.2 Creating a Pull Request

1. **Push your branch to GitHub:**
   ```bash
   git push origin feature-xyz
   ```

2. **Open a Pull Request:**
   - Go to your repository on GitHub.
   - You’ll often see a banner to “Compare & pull request” for recently pushed branches.
   - Or, click the “Pull requests” tab, then “New pull request”.
   - Select the base branch (e.g., `main`) and your compare branch (e.g., `feature-xyz`).
   - Write a clear title and description (explain what, why, and any special notes).

---

## 6.3 Reviewing Code

- **Reviewers** can leave comments on lines of code, suggest changes, and approve or request changes.
- Aim for clear, constructive feedback—focus on code quality, style, security, and maintainability.
- Respond to comments, make improvements, and push more commits to your branch if needed.

---

## 6.4 Merging a Pull Request

When your PR is approved:
- Click “Merge pull request” on GitHub.
- Choose “Create a merge commit”, “Squash and merge”, or “Rebase and merge” according to your team’s workflow.
- Delete the source branch after merging to keep the repo clean.

---

## 6.5 Keeping Your PR Up to Date

If the base branch has changed since you started your PR:
1. Update your feature branch locally:
   ```bash
   git checkout feature-xyz
   git fetch origin
   git rebase origin/main
   ```
   or:
   ```bash
   git merge origin/main
   ```
2. Resolve any conflicts, commit, and push changes:
   ```bash
   git push origin feature-xyz
   ```

---

## 6.6 Pull Request Best Practices

- Make PRs small and focused (easier to review, less likely to conflict).
- Provide a clear description and context.
- Respond promptly to feedback.
- Use draft PRs for work in progress.
- Link issues the PR addresses (e.g., “Closes #42”).
- Run tests and check CI results before merging.

---

## 6.7 Example Workflow

1. Create a new branch for your feature:
   ```bash
   git switch -c feature-login
   ```
2. Make your code changes, add, and commit:
   ```bash
   git add .
   git commit -m "Add login feature"
   ```
3. Push your branch:
   ```bash
   git push -u origin feature-login
   ```
4. Open a Pull Request on GitHub.
5. Collaborate through review and discussion.
6. Merge when approved.

---

## 6.8 Summary Table

| Action                     | Command/Location              |
|----------------------------|-------------------------------|
| Push branch to GitHub      | `git push origin <branch>`    |
| Open PR                    | GitHub website                |
| Review PR                  | GitHub website                |
| Merge PR                   | GitHub website                |
| Keep PR up to date         | `git rebase` / `git merge`    |

---

**Next:** Industry best practices—commit messages, branch naming, `.gitignore`, and more!