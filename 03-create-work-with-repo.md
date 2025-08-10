# 3. Creating and Working With Your First Repository

Now let’s create your first Git repository, add files, make commits, and connect it to GitHub. This will help you understand the basic flow of using Git as a developer.

---

## 3.1 Creating a New Local Repository

Navigate to the folder where you want your project to live, then run:

```bash
mkdir my-first-repo
cd my-first-repo
git init
```

- `git init` creates a new, empty Git repository in your current directory.
- After this, a hidden `.git` folder appears (contains all Git’s internal data).

---

## 3.2 Adding Files and Making Your First Commit

1. **Create a file:**

   ```bash
   echo "Hello, Git!" > hello.txt
   ```

2. **Check the status:**

   ```bash
   git status
   ```
   - You’ll see `hello.txt` as “untracked”.

3. **Stage the file (add to the staging area):**

   ```bash
   git add hello.txt
   ```

4. **Check status again:**

   ```bash
   git status
   ```
   - Now `hello.txt` is in the staging area.

5. **Commit the file:**

   ```bash
   git commit -m "Add hello.txt with greeting"
   ```
   - Commits take everything in the staging area and snapshot it in your project history with a message.

---

## 3.3 Viewing Commit History

See your commit log:

```bash
git log
```

- Shows commit hash, author, date, and message.
- Press `q` to quit the log view.

---

## 3.4 Connecting to GitHub: Create a Remote Repository

1. Go to [GitHub](https://github.com/) and click “New repository”.
2. Name it (e.g., `my-first-repo`). DON’T initialize with a README, .gitignore, or license.
3. After creation, GitHub shows instructions for pushing an existing repo.

**Follow these steps in your terminal:**

```bash
git remote add origin git@github.com:<your-username>/my-first-repo.git
git branch -M main
git push -u origin main
```

- `git remote add origin ...` connects your local repo to GitHub.
- `git branch -M main` renames your branch to `main` (standard practice).
- `git push -u origin main` uploads your commits to GitHub and sets up tracking.

---

## 3.5 Cloning an Existing Repository

To copy (clone) a repository from GitHub to your computer:

```bash
git clone git@github.com:<some-user>/<some-repo>.git
```
- This creates a local copy with the remote already set.

---

## 3.6 Summary Table

| Command                        | Purpose                                      |
|--------------------------------|----------------------------------------------|
| `git init`                     | Create a new local repository                |
| `git add <file>`               | Stage a file for commit                      |
| `git commit -m "message"`      | Commit staged changes                        |
| `git status`                   | Show current repo status                     |
| `git log`                      | Show commit history                          |
| `git remote add origin <url>`  | Link local repo to remote (GitHub)           |
| `git push -u origin main`      | Push commits to GitHub and track the branch  |
| `git clone <url>`              | Copy a remote repo to your local machine     |

---

**You now have a working local and remote repository!**

---

Next: [Branching and merging—work on features independently and combine changes safely.](./04-branching-and-merging.md)
