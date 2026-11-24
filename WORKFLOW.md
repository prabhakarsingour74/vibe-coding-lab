# GitHub Workflow: Public Index + Independent Projects

This repository is the public directory. Every actual project has its own GitHub repository and its own visibility setting.

## 1. Create a project locally

Create a separate folder **outside** this master repository.

```bash
mkdir my-new-project
cd my-new-project
git init
```

Add source code, a project README, `.gitignore`, and `.env.example` as needed. Never add real credentials or `.env`.

## 2. Create its GitHub repository

On GitHub, choose **New repository**:

- Choose a descriptive project name.
- Select **Private** while experimenting if you do not want the code public.
- Select **Public** if you are ready for anyone to view and clone it.
- If you already have local files, do not initialize the remote with another README, license, or `.gitignore`.

Visibility belongs to the individual project repository. It is independent of this public index.

## 3. Push the project

Copy the remote URL from GitHub and run:

```bash
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/my-new-project.git
git push -u origin main
```

## 4. Add a public project to this index

Only do this after the project's repository is public and you are comfortable sharing its name and description.

1. Open the matching category's `README.md`.
2. Add a row with project name, concise description, status, repository URL, and optional demo.
3. Add screenshots or a project card only if useful.
4. Commit and push the update to `vibe-coding-lab`.

Example:

```markdown
| [Project Name](https://github.com/YOUR_USERNAME/project-name) | AI | Short description | Prototype | [GitHub](https://github.com/YOUR_USERNAME/project-name) | [Demo](https://example.com) |
```

Replace all example values with real details. Do not publish private project links or metadata unless you intend to disclose them.

## 5. Make a private project public later

1. Review code, configuration, commit history, branches, tags, releases, issues, wiki, and GitHub Actions logs.
2. Remove secrets and confidential data. Rotate any credential that was ever committed; deleting it in a later commit is not enough.
3. Check third-party code, datasets, assets, and licenses.
4. In the project's GitHub repository, open **Settings → General → Danger Zone → Change repository visibility**.
5. Choose **Make public** and confirm after reading GitHub's warning.
6. Add it to this public index if you want it showcased.

## 6. Keep the repositories separate

- Do not put a private project's folder inside this public repository.
- Do not copy private source code here.
- The master repository stores public links and descriptions only.
- A project can remain private forever and never appear in this index.

## 7. Day-to-day commands

Run these inside the project repository you are working on:

```bash
git status
git add .
git commit -m "Describe the change"
git push
```

## Suggested project names

- `ai-resume-builder`
- `local-rag-playground`
- `browser-task-automator`
- `portfolio-interaction-lab`

Prefer clear names over `test2`, `new-final`, or `project-latest`.
