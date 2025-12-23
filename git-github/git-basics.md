# 🧠 Git & GitHub Fundamentals

Git and GitHub are **essential tools in DevOps**.  
They enable **version control, collaboration, automation, and CI/CD workflows**.

---

## 🧩 What is Git?

**Git** is a **distributed version control system** that allows you to:

- Track changes in source code
- Collaborate with other developers
- Revert to previous versions
- Work safely in parallel using branches

![Git Version Control Diagram](https://upload.wikimedia.org/wikipedia/commons/e/e0/Git-logo.svg)

### 🔑 Key Characteristics of Git
- Distributed (each developer has a full copy)
- Fast and reliable
- Works offline
- Widely used in DevOps pipelines

---

## 🌐 What is GitHub?

**GitHub** is a **cloud platform** that hosts Git repositories and adds collaboration features such as:

- Pull Requests
- Issues & Projects
- GitHub Actions (CI/CD)
- Code reviews

![GitHub Workflow Diagram](https://docs.github.com/assets/images/help/repository/workflow-basic.png)

---

## 🔄 Git vs GitHub

| Git | GitHub |
|----|-------|
| Version control system | Hosting & collaboration platform |
| Works locally | Cloud-based |
| Command-line tool | Web interface + automation |
| Tracks code changes | Manages teams & workflows |

---

## 🧠 Basic Git Concepts

### 📁 Repository
A repository (repo) is a **project folder tracked by Git**.

### 💾 Commit
A commit is a **snapshot of changes** with a message.

### 🌿 Branch
A branch allows you to work on features **without breaking main code**.

### 🔀 Merge
Merge combines changes from one branch into another.

![Git Branching Diagram](https://upload.wikimedia.org/wikipedia/commons/3/3f/Git_branching.svg)

---

## ⌨️ Essential Git Commands

```bash
git init              # Initialize a repository
git status            # Check repository state
git add .             # Stage changes
git commit -m "msg"   # Save changes
git branch            # List branches
git checkout -b dev   # Create & switch branch
git merge dev         # Merge branch
git push              # Upload to GitHub
git pull              # Download updates
```
---

## 🔁 Git Workflow (Typical DevOps Flow)

- Clone repository

- Create feature branch

- Make changes

- Commit changes

- Push to GitHub

- Open Pull Request

- Review & Merge

- CI/CD pipeline runs automatically
