# Git + Docker Sprint Â· `git-docker-sprint`
[![Secret Scan](https://github.com/KatieBarnes147/git-docker-sprint/actions/workflows/secret-scan.yml/badge.svg)](https://github.com/KatieBarnes147/git-docker-sprint/actions/workflows/secret-scan.yml)

This project demonstrates version control best practices with **Git/GitLab** and containerization using **Docker Compose**.  
Originally developed for graduate coursework, now polished for portfolio showcase.

---

## ðŸŽ¯ Project Overview
The goal was to apply core **Git workflow** skills (branching, merging, reverting, closing issues via commit messages) while also learning how to **containerize a simple Python app** and run it with **Docker Compose**.

**Key deliverables**
- Implemented a `doubleIt` function in Python
- Managed branches and resolved merge conflicts
- Used `git revert` to preserve history while correcting mistakes
- Built/running a container with a success page
- Auto-closed issues via commit messages
- Wrote a sprint reflection in Markdown

---

## ðŸ”§ Tech Stack
- **Git & GitLab/GitHub** (version control, merge requests/PRs)
- **Python 3** (app logic)
- **Docker & Docker Compose** (containerization)
- **Markdown** (documentation & sprint reflection)

---

## ðŸš€ Quick Start

### Prerequisites
- Docker Desktop (or Docker Engine + Compose)
- Python 3 (optional if you want to run locally without Docker)

### Setup Environment
**PowerShell (Windows)**
```powershell
Copy-Item .env.example .env
```
**bash (macOS/Linux/Git Bash)**
```bash
cp .env.example .env
```
You can keep the defaults (`PORT=5000`).

### Run with Docker
```bash
docker compose up --build
# If you have the older plugin:
# docker-compose up --build
```
Then open **http://localhost:5000** ðŸŽ‰

### Run locally (no Docker)
```bash
pip install -r requirements.txt
python app.py
```

---

## ðŸ–¼ï¸ Live Demo

---

## ðŸ“š What I Learned
- Confidently using **git revert** to fix mistakes without rewriting history  
- Handling **merge conflicts** step-by-step  
- **Auto-closing issues** with commit messages (`Fixes #123`)  
- Containerizing a Python app with a minimal **Compose** setup  
- Maintaining clean repos with **.gitignore** and **.env.example**

---

## ðŸ”’ Security
This repo is sanitized; **no real secrets are committed**.

- Real `.env` files are **ignored**
- Example config lives in **`.env.example`** (safe placeholders)
- **Server-side scanning:** Gitleaks runs on every push/PR via GitHub Actions
- Optional local scan anytime:

**PowerShell**
```powershell
docker run --rm -v "$($PWD.Path):/repo" -w /repo zricethezav/gitleaks:latest detect --no-git --redact
```

**bash**
```bash
docker run --rm -v "$PWD:/repo" -w /repo zricethezav/gitleaks:latest detect --no-git --redact
```

---

## ðŸ—‚ï¸ Project Structure (minimal)
```
.
â”œâ”€ app.py              # simple Python endpoint / success page
â”œâ”€ requirements.txt    # Flask dependency
â”œâ”€ docker-compose.yml  # compose service definition
â”œâ”€ Dockerfile          # image build for the app
â”œâ”€ .env.example        # safe placeholders
â”œâ”€ README.md
â””â”€ docs/
   â””â”€ success.png      # screenshot used in the README
```

---

## ðŸ¤” Next Steps
- Add a basic CI job to run unit tests (pytest)  
- Expand the app beyond a simple success page  
- Explore CI/CD pipelines (GitHub Actions or GitLab Auto DevOps)

---

## âœï¸ Author
**Katie Barnes** â€” M.S. Computer Science & Software Engineering  
GitHub: [@katiebarnes147](https://github.com/katiebarnes147) 




