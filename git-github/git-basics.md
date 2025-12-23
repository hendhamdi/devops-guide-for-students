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

![GitHub Pull Request Workflow](https://enggkatta.com/wp-content/uploads/2024/06/introduction-to-github-800x445.jpg)

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

![Git Branching]([../resources/images/git-basics/Basic-Git-Concepts.png](https://lh3.googleusercontent.com/gg-dl/ABS2GSlcWCk6-XxVmhg8GpI1_-hg22tdBWCf4K_XuISO1r5vJ10egwKzDuh_zwq5dceQB5pF8nYulu4sEZzYmcXH3ONpZ0muXsSiJPzYg3kdU2HAsaQ_KoGqxIZ3QH4Linvr0drugDiJMGEn8H6qUN2cIh7q5XqeamcQcFS_JQfcXWGcRndTaw=s1024-rj) "Git Branching Diagram")

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

![Git Workflow](../resources/images/git-basics/Git-Workflow.png "Git Workflow Diagram")

  ---

  ## 🚀 Why Git & GitHub Matter in DevOps

- Enable CI/CD pipelines

- Improve team collaboration

- Ensure traceability & rollback

- Automate testing & deployment

- Foundation of Infrastructure as Code

---

## 📌 Summary

Git manages code versions locally
GitHub enables collaboration, automation, and DevOps pipelines

Together, they are the backbone of modern DevOps practices.



➡️ Next step in learning:

`ci-cd/ci-cd-basics.md` → CI/CD concepts & pipelines
