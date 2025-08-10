# 2. Setting Up Git & GitHub

In this step, you’ll set up everything you need to start using Git and GitHub as a developer. This includes installing Git, configuring your identity, setting up secure authentication with GitHub, and creating your GitHub account.

---

## 2.1 Installing Git

**Windows:**
- Download from [git-scm.com](https://git-scm.com/download/win)
- Run the installer and follow the prompts (default settings are usually fine).

**Mac:**
- Use Homebrew:  
  ```bash
  brew install git
  ```
- Or download the installer from [git-scm.com](https://git-scm.com/download/mac)

**Linux:**
- For Ubuntu/Debian:  
  ```bash
  sudo apt update
  sudo apt install git
  ```
- For Fedora:  
  ```bash
  sudo dnf install git
  ```

---

## 2.2 Configuring Git (Your Identity)

Set your name and email (these appear in your commits):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
**Tip:** Use the same email as registered on GitHub for full integration.

Set your preferred default editor (optional):

```bash
git config --global core.editor "code --wait"   # VS Code
git config --global core.editor "nano"          # Nano editor
```

See all your config settings:

```bash
git config --list
```

---

## 2.3 Creating a GitHub Account

1. Go to [github.com](https://github.com/) and sign up.
2. Verify your email address.
3. (Optional but recommended) Enable two-factor authentication (2FA) for security.

---

## 2.4 Setting Up SSH Keys for Secure Authentication

Instead of typing your GitHub password every time, use SSH keys.

### Generate an SSH key:
```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
# Press Enter to accept the default file location and set a passphrase if you want.
```
This creates public (`id_ed25519.pub`) and private (`id_ed25519`) keys in `~/.ssh/`.

### Add your SSH key to the SSH agent:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### Add your public key to GitHub:

- Copy your public key:
  ```bash
  cat ~/.ssh/id_ed25519.pub
  ```
- On GitHub, go to **Settings > SSH and GPG keys > New SSH key**.
- Paste the key and save.

---

## 2.5 Checking Your Setup

Test connection:

```bash
ssh -T git@github.com
```
You should see:  
`Hi <your-username>! You've successfully authenticated...`

---

## 2.6 Configure GitHub Username in Git (Optional)

If you want your GitHub username to show in some CLI actions:

```bash
git config --global github.user <your-github-username>
```

---

## 2.7 Quick Recap

- You have Git installed and configured.
- You’ve set up SSH keys for secure GitHub access.
- Your GitHub account is ready.

**Next:** Creating and working with your first repository!