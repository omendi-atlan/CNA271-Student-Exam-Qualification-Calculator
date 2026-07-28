# GitHub Repository Setup Guide

This folder is already a fully initialized Git repository on the `main` branch with one clean initial commit.

Follow these steps to publish it on GitHub.

---

## 1. Create a new repository on GitHub

1. Go to [https://github.com/new](https://github.com/new)
2. Repository name recommendation:  
   `CNA271-Student-Exam-Qualification-Calculator`
3. Description:  
   `CNA271 Project – Containerized Student Exam Qualification Calculator + full group presentation package`
4. Set visibility to **Public** (recommended so the lecturer can easily access it)
5. **Do NOT** initialize with a README, .gitignore, or license (we already have them)
6. Click **Create repository**

---

## 2. Connect this local repository and push

Open a terminal in this folder and run the commands GitHub shows you (they will look like this):

```bash
git remote add origin https://github.com/YOUR-USERNAME/CNA271-Student-Exam-Qualification-Calculator.git
git push -u origin main
```

Replace `YOUR-USERNAME` with the actual GitHub username (or organization).

If you prefer SSH:

```bash
git remote add origin git@github.com:YOUR-USERNAME/CNA271-Student-Exam-Qualification-Calculator.git
git push -u origin main
```

---

## 3. Optional but recommended improvements

### Add collaborators (all group members)
- Go to the repository → Settings → Collaborators → Add people

### Pin the repository or add topics
Suggested topics: `cna271`, `docker`, `dotnet`, `microservices`, `cloud-native`, `belgium-campus`

### Update the Docker Hub link
If the Docker Hub username is different from `reneumbra`, edit these files:
- `README.md`
- `docs/presentation/05-Docker-Hub-Deployment.md`
- `docs/presentation/Speaker-Notes.md`
- `PROJECT-README.md`

Then commit and push:

```bash
git add .
git commit -m "Update Docker Hub image name"
git push
```

---

## 4. How the group should use the repository on presentation day

1. Open the GitHub repository in a browser.
2. Navigate to `docs/presentation/`.
3. Follow the numbered files in order.
4. Use `Speaker-Notes.md` for exact speaking scripts.
5. For the live demo, open a terminal and run:

```bash
docker pull reneumbra/student-exam-app:latest
docker run -it --rm reneumbra/student-exam-app:latest
```

---

## Current repository status

- Branch: `main`
- Initial commit already created
- Working tree is clean
- Ready to push

You only need to create the empty repo on GitHub and run the two `git remote` + `git push` commands.
