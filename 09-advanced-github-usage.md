# 9. Advanced GitHub Usage

As you grow as a developer, GitHub offers advanced features for automation, security, documentation, and collaboration. Mastering these tools will help you work more efficiently and professionally.

---

## 9.1 GitHub Actions: Automation and CI/CD

**GitHub Actions** allows you to automate workflows, such as running tests, building your app, or deploying code, every time you push or open a pull request.

- **Basic Workflow Example:** `.github/workflows/ci.yml`
  ```yaml
  name: CI
  on: [push, pull_request]
  jobs:
    build:
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v4
        - name: Set up Node.js
          uses: actions/setup-node@v4
          with:
            node-version: 20
        - run: npm install
        - run: npm test
  ```
- Explore ready-made Actions in the [GitHub Marketplace](https://github.com/marketplace?type=actions).

---

## 9.2 Managing Secrets and Environment Variables

- Store sensitive information (API keys, credentials) securely in **GitHub Secrets**.
- Access them in Actions workflows like this:
  ```yaml
  env:
    API_KEY: ${{ secrets.API_KEY }}
  ```

---

## 9.3 GitHub Packages and Registries

- Host and manage packages (npm, Docker, Maven, etc.) using [GitHub Packages](https://docs.github.com/en/packages).
- Example: Publish a Node package to GitHub Packages by following the setup in your repo and workflow.

---

## 9.4 GitHub Pages: Documentation and Websites

- Host static websites or docs directly from your repo.
- To enable, go to **Settings > Pages**, select a branch/folder, and GitHub builds your site.
- Common for project documentation using Markdown and static site generators (Jekyll, Docusaurus, etc.).

---

## 9.5 Managing Teams and Permissions

- Use organizations and teams for project collaboration.
- Assign roles (Admin, Write, Read) and manage access at the repo/team level.
- Use branch protection rules to enforce code reviews and status checks.

---

## 9.6 Security Best Practices

- **Dependabot**: Automates dependency updates and security alerts.
- **Secret scanning**: Detects accidentally committed secrets.
- **Code scanning**: Finds security issues in your codebase.
- Enable these features in your repo’s **Security** settings.

---

## 9.7 Using GitHub Discussions

- Enable **Discussions** for Q&A, ideas, or feedback.
- Good for community-driven projects or open source collaboration.

---

## 9.8 Example: Setting Up a Simple CI Workflow

1. Create a file at `.github/workflows/ci.yml` in your repo.
2. Add the following:
    ```yaml
    name: CI
    on: [push, pull_request]
    jobs:
      test:
        runs-on: ubuntu-latest
        steps:
          - uses: actions/checkout@v4
          - run: echo "Your tests go here!"
    ```
3. Commit and push. GitHub will run the workflow for every push or PR.

---

## 9.9 Summary Table

| Feature                | Benefit                                      |
|------------------------|----------------------------------------------|
| GitHub Actions         | Automation, CI/CD                            |
| Secrets                | Secure storage of credentials                |
| Packages               | Manage and distribute dependencies           |
| Pages                  | Host project websites/docs                   |
| Teams/Permissions      | Controlled collaboration                     |
| Security tools         | Safer, more secure code                      |
| Discussions            | Community engagement                         |

---

Next: [Open source and community collaboration—how to contribute, fork, and work within the open-source ecosystem!](./10-open-source-contribution.md)
