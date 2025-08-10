# Comprehensive Guide: Git + GitHub + Industry Practices for Developers

## 1. Introduction
- What is Git?  
- What is GitHub?  
- Why version control is essential for developers  
- Typical developer workflow overview: local development, collaboration, CI/CD

---

## 2. Setting Up Git & GitHub
- Installing Git (Windows, Mac, Linux)
- Setting up basic Git configuration (user.name, user.email, default editor)
- Generating and adding SSH keys to GitHub
- Creating a GitHub account and configuring 2FA

---

## 3. Your First Repository
- Initializing a local repository (`git init`)
- Cloning a remote repository (`git clone`)
- Understanding the working directory, staging area, and git repository
- Adding and committing files (`git add`, `git commit`)
- Viewing history (`git log`, `git show`)

---

## 4. Branching and Merging
- What are branches and why use them?
- Creating and switching branches (`git branch`, `git checkout`, `git switch`)
- Merging branches (`git merge`)
- Fast-forward vs. non-fast-forward merges
- Resolving merge conflicts

---

## 5. Working with Remotes
- Connecting to GitHub remotes (`git remote add`, `git remote -v`)
- Pushing and pulling changes (`git push`, `git pull`)
- Fetching changes (`git fetch`)
- Forking and contributing to open source projects

---

## 6. Collaboration Workflows
- Feature branching workflow
- Pull Requests: creating, reviewing, and merging on GitHub
- Code review best practices (clear comments, approvals, requesting changes)
- Keeping your fork/branch up to date (`git fetch upstream`, `git rebase` or `git merge`)
- Resolving conflicts in collaborative environments

---

## 7. Commit Best Practices
- Writing clear, meaningful commit messages (conventional commits, why it matters)
- Small, atomic commits for easier review and rollback
- Using `.gitignore` to avoid committing unnecessary files
- Amending commits and interactive rebase for clean history

---

## 8. Advanced Git for Developers
- Stashing changes (`git stash`)
- Cherry-picking commits (`git cherry-pick`)
- Squashing commits during PRs (`git rebase -i`)
- Bisecting to find bugs (`git bisect`)
- Undoing mistakes (`git reset`, `git revert`, `git reflog`)

---

## 9. Leveraging GitHub Features
- Issues and project boards for tracking work
- Using labels, milestones, and assignees
- Branch protection rules and required reviews
- Setting up and using GitHub Actions for CI/CD
- Managing secrets and environment variables for deployments
- Using GitHub Packages, Releases, and Tags

---

## 10. Security and Code Quality
- Keeping dependencies up to date with Dependabot
- Enabling security features: secret scanning, code scanning, vulnerability alerts
- Enforcing code style and using linters in CI
- Reviewing and managing access permissions in repositories

---

## 11. Open Source Contribution (as a Developer)
- Finding good first issues
- Forking and cloning repositories
- Setting upstream remotes and keeping your fork up to date
- Submitting effective Pull Requests with good descriptions
- Following project contribution guidelines and CODEOWNERS
- Understanding licensing and Contributor License Agreements (CLAs)

---

## 12. Troubleshooting & Recovery
- Recovering lost commits/branches with `git reflog`
- Handling detached HEAD state
- Resolving complex merge and rebase conflicts
- Cleaning large files and sensitive data from history (BFG, filter-branch)

---

## 13. Continuous Improvement
- Following GitHub’s official documentation and guides
- Recommended books, courses, and cheat sheets
- Joining developer communities and discussions

---

## 14. Appendix
- Common Git and GitHub command cheat sheet
- Example `.gitignore` for various languages
- Example Pull Request and Issue templates
- Useful Git/GitHub configuration and aliases

---

## 15. End-to-End Example: Typical Developer Workflow
1. Clone a repository
2. Create a feature branch
3. Make changes and commit
4. Push branch and open a Pull Request
5. Review, resolve conflicts, and merge
6. Clean up branches locally and remotely

---

Start: [01 Introduction Git Github For Developers](./01-introduction-git-github-for-developers.md)
