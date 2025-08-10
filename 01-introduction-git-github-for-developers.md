# 1. Introduction to Git & GitHub for Developers

Welcome! In this section, you'll learn what Git and GitHub are, why they're essential for developers, and get an overview of the typical workflow. We'll also introduce the basic syntax and terminology you'll encounter.

---

## What is Git?

**Git** is a distributed version control system that lets you:
- Track changes in your codebase over time.
- Collaborate with other developers safely.
- Revert to previous versions if you make mistakes.

**Key Benefits:**
- **History:** Every change is recorded, so you can see who changed what and when.
- **Collaboration:** Multiple people can work on the same project without interfering with each other.
- **Branching:** Try new ideas without breaking the main codebase.

---

## What is GitHub?

**GitHub** is a platform that hosts Git repositories online and offers tools for collaboration, code review, issue tracking, and automation.

**Key Features:**
- Remote storage for your Git repositories.
- Tools for Pull Requests, Issues, and Discussions.
- Integration with CI/CD, project management, and security.
- Social coding (share, contribute, discover projects).

---

## Why Do Developers Use Git & GitHub?

- **Backup:** Your code is safe and versioned in the cloud.
- **Teamwork:** Work with others via branches, pull requests, and code review.
- **Open Source:** Discover, contribute to, and learn from public projects.
- **Automation:** Run tests and deployments automatically.

---

## The Developer Workflow (Quick Overview)

1. **Clone**: Get a copy of a remote repository.
2. **Branch**: Create a separate line of development.
3. **Commit**: Save your changes locally with a message.
4. **Push**: Upload your commits to GitHub.
5. **Pull Request (PR)**: Propose your changes for review and merging.
6. **Merge**: Integrate your changes into the main branch.

---

## Basic Git Syntax and Concepts

Here are core terms and example commands you’ll use daily:

| Term          | Description                                    | Example Command / Syntax                   |
|---------------|------------------------------------------------|---------------------------------------------|
| Repository (repo) | A project tracked by Git.                    | `git init` (create), `git clone URL` (copy) |
| Commit        | A snapshot of your changes.                    | `git commit -m "message"`                   |
| Branch        | A separate line of development.                | `git branch feature-x`<br>`git checkout feature-x` |
| Merge         | Combine changes from different branches.        | `git merge branch-name`                     |
| Push          | Upload commits to GitHub.                      | `git push origin branch-name`               |
| Pull          | Download changes from GitHub.                  | `git pull origin branch-name`               |
| Status        | Show current state of working directory.       | `git status`                                |
| Log           | Show commit history.                           | `git log`                                   |

---

## Example: Creating and Saving Changes

```bash
# Initialize a new repo
git init

# Check status
git status

# Add a file to the staging area
git add myfile.py

# Commit the changes
git commit -m "Add myfile.py with initial code"
```

---

## Summary

- **Git** tracks your code history and changes.
- **GitHub** lets you store, share, and collaborate on Git repositories online.
- Developers use both to work safely and efficiently, whether solo or in teams.

**Next:** Setting up your environment for Git & GitHub!