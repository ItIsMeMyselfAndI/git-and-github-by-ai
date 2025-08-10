# 10. Open Source and Community Collaboration

Contributing to open source projects is a great way to learn, build your reputation, and give back to the community. Git and GitHub make this process efficient and transparent.

---

## 10.1 Finding Projects to Contribute To

- Use [GitHub Explore](https://github.com/explore) or search for topics you care about.
- Look for repositories labeled with `good first issue`, `help wanted`, or `beginner friendly`.
- Read the README, CONTRIBUTING.md, and project documentation to understand the rules and setup.

---

## 10.2 Forking and Cloning

To contribute, you typically **fork** (copy) the repository to your account, then clone it locally:

```bash
# On GitHub: Click "Fork" on the repo page
# On your computer:
git clone git@github.com:your-username/project-name.git
cd project-name
```

---

## 10.3 Setting Up Remotes

Add the original repo as an `upstream` remote to keep your fork up to date:

```bash
git remote add upstream git@github.com:original-owner/project-name.git
```

---

## 10.4 Keeping Your Fork Up to Date

Regularly sync your fork with the upstream project:

```bash
git fetch upstream
git checkout main
git merge upstream/main
# Or, to rebase:
git rebase upstream/main
git push origin main
```

---

## 10.5 Making Your Contribution

1. **Create a branch for your fix or feature:**
   ```bash
   git switch -c fix-spelling-error
   ```

2. **Make and commit your changes:**
   ```bash
   git add .
   git commit -m "fix(docs): correct spelling in README"
   ```

3. **Push your branch to your fork:**
   ```bash
   git push origin fix-spelling-error
   ```

---

## 10.6 Submitting a Pull Request

- Go to your fork on GitHub.
- Click “Compare & pull request” or go to the “Pull Requests” tab and click “New pull request”.
- Select your branch and target the original repo’s default branch (often `main`).
- Fill out the PR template, describe your changes, and link any relevant issues.
- Be responsive to feedback and update your PR as needed.

---

## 10.7 Following Contribution Guidelines

- Always check for a `CONTRIBUTING.md` file.
- Follow coding standards, commit message conventions, and testing requirements.
- Some projects require you to sign a Contributor License Agreement (CLA).

---

## 10.8 Understanding Licensing

- Respect the project’s license (MIT, GPL, Apache, etc.).
- Your contributions are typically covered by the same license.

---

## 10.9 Summary Table

| Step                          | Command / Action                           |
|-------------------------------|--------------------------------------------|
| Fork a repo                   | Click "Fork" on GitHub                     |
| Clone your fork               | `git clone git@github.com:you/repo.git`    |
| Add upstream remote           | `git remote add upstream ...`              |
| Sync with upstream            | `git fetch upstream` + `git merge/rebase`  |
| Make a branch for your work   | `git switch -c branch-name`                |
| Push your branch              | `git push origin branch-name`              |
| Open a Pull Request           | On GitHub website                          |
| Follow guidelines             | Read `CONTRIBUTING.md`, respect licenses   |

---

Next: [Troubleshooting and recovery—how to fix mistakes, recover lost work, and handle common Git pitfalls!](./11-git-troubleshooting-and-recovery.md)
