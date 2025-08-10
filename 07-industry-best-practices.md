# 7. Industry Best Practices for Git & GitHub

Adopting industry best practices helps teams write cleaner code, avoid common mistakes, and collaborate efficiently. Here are essential habits every developer should follow with Git and GitHub.

---

## 7.1 Writing Great Commit Messages

- **Be concise and descriptive**:  
  Good: `Fix login redirect bug`  
  Bad: `fixed stuff`
- **Follow the conventional format** (recommended):  
  ```
  <type>(optional scope): <short summary>
  <blank line>
  <detailed explanation, if necessary>
  ```
  Example:  
  ```
  feat(auth): add JWT authentication

  Implements JWT auth for API endpoints. Updates user model and docs.
  ```

- **Types**: feat, fix, docs, style, refactor, test, chore, etc.

---

## 7.2 Committing Early and Often

- Commit small, logical changes.
- Each commit should represent a single purpose or fix.
- Avoid large, monolithic commits that mix unrelated changes.

---

## 7.3 Branch Naming Conventions

- Use clear, descriptive names:
  - `feature/login-form`
  - `fix/navbar-alignment`
  - `chore/update-deps`

- Prefer hyphens or slashes to separate words.

---

## 7.4 Using `.gitignore` Effectively

- Use a `.gitignore` file to exclude files and folders that shouldn’t be tracked (e.g., `node_modules`, `.env`, build artifacts).
- Example for a Node project:
  ```
  node_modules/
  .env
  dist/
  ```

- [Find templates for popular languages](https://github.com/github/gitignore).

---

## 7.5 Keeping `main` Deployable

- Never commit broken or experimental code to `main`.
- Use branches and Pull Requests for all changes.
- Protect `main` with branch protection rules and required reviews.

---

## 7.6 Pull Request and Issue Templates

- Use templates to standardize PR and issue submissions.
- Example PR template:
  ```
  ## What does this PR do?

  ## How to test

  ## Related issues
  ```

- Place templates in `.github/` directory in your repo.

---

## 7.7 Semantic Versioning and Releases

- Tag releases using semantic versioning (`v1.2.3`) to track and communicate changes.
- Use annotated tags:
  ```bash
  git tag -a v1.2.3 -m "Release version 1.2.3"
  git push origin v1.2.3
  ```

---

## 7.8 Code Reviews

- Review all Pull Requests before merging.
- Use GitHub’s “Request changes” and “Approve” features.
- Leave clear, constructive comments.
- Check for: code quality, security, tests, documentation.

---

## 7.9 Continuous Integration (CI)

- Set up GitHub Actions (or similar) to run automatic tests, linting, and builds on every PR.
- Prevent merging if CI fails.

---

## 7.10 Keeping Dependencies and Code Secure

- Use Dependabot to automate dependency updates.
- Enable GitHub’s security features: secret scanning, code scanning, vulnerability alerts.

---

## 7.11 Summary Table

| Practice                        | Why It Matters                            |
|----------------------------------|-------------------------------------------|
| Good commit messages             | Easier history & collaboration            |
| Small, focused commits           | Easier reviews & rollbacks                |
| Descriptive branch names         | Clear context for teammates               |
| Use `.gitignore`                 | Avoid committing sensitive/junk files     |
| PR/issue templates               | Consistent, clear communication           |
| Semantic versioning/releases     | Track changes for users & teammates       |
| Code reviews                     | Improved quality & shared knowledge       |
| CI/CD                            | Catch bugs early, automate deployment     |
| Security features                | Prevent vulnerabilities                   |

---

Next: [Advanced Git—interactive rebase, cherry-pick, stash, bisect, and more!](./08-advanced-git-for-developers.md)
