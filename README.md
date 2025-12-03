#  Fusion Workflow

**Fusion Workflow** is a foundational project designed to establish a fully professional development workflow using Python, Git, pre-commit, and GitHub Actions.
This repository represents **Stage 0** of the Data Engineering / Data Science Roadmap and serves as the technical base for all future projects.

---

##  Project Purpose

This project sets up a modern, production-grade engineering workflow with:

- Git Flow (feature → develop → main)
- Automated hooks using **pre-commit**
- A CI/CD pipeline with **GitHub Actions**
- Unit testing with `pytest`
- Python linting + formatting standards (Black + pre-commit)

This repository is intended to be a **template** for upcoming projects involving:

- ETL / ELT pipelines
- Data orchestration (Airflow)
- Data modeling (dbt)
- MLOps
- Machine Learning
- Data Science

---

#  Project Structure
fusion-workflow/
│
├── .github/workflows/
│ └── python-ci.yml # CI/CD: lint + tests
│
├── src/
│ └── example.py # Example module
│
├── tests/
│ └── test_example.py # Unit testing example
│
├── .pre-commit-config.yaml # Pre-commit hooks
├── requirements.txt # Initial dependencies
└── README.md

---

# Installation & Setup

### 1. Create virtual environment

```bash
python3 -m venv venv
source venv/bin/activate

### 2. Install dependencies
pip install -r requirements.txt

### 3. Install pre-commit
pip install pre-commit
pre-commit install

###4. Run tests
pytest -q

---

#Pre-commit Hooks Included

The following hooks run automatically on every commit:

Trim trailing whitespace

Fix end-of-file newline

Check YAML syntax

Detect large files

Black formatter (PEP8 auto-formatting)

Run them manually:

pre-commit run --all-files


---

#CI/CD with GitHub Actions

The pipeline python-ci.yml automatically performs:

Install dependencies

Run linting and Black formatting

Run pytest

Report CI status in Pull Requests

Triggered on push or PR to:

develop
main


---

#Unit Testing Example

Example function:

def add(a: int, b: int) -> int:
    return a + b


Associated test:

def test_add():
    assert add(2, 3) == 5

---

# Git Branching Model (Git Flow)
feature/* → develop → main

# Example usage
git checkout -b feature/new-feature
# work…
git push -u origin feature/new-feature
gh pr create --base develop --head feature/new-feature
