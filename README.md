# Fusion Workflow

Fusion Workflow es el entorno base para construir pipelines de datos, ETLs, orquestación y automatización CI/CD siguiendo buenas prácticas utilizadas en equipos de Data Engineering de nivel enterprise.

Este repositorio forma parte del Roadmap Profesional 2025–2026 (Data Engineer Senior).

---

##  Objetivo del Proyecto

Establecer una base sólida de:
- Control de versiones (Git + GitHub)
- Automatización CI/CD con GitHub Actions
- Estándares de calidad: linters, formateo y pruebas
- Estructura profesional para futuros módulos ETL, pipelines y servicios

---

## Estructura del Proyecto

fusion-workflow/
├── .github/workflows/ # Pipelines CI/CD
│ └── python-ci.yml
├── .pre-commit-config.yaml # Formateo, linting y validaciones
├── src/ # Código fuente
│ └── example.py
├── tests/ # Pruebas unitarias con pytest
│ └── test_example.py
└── README.md # Documentación principal

---

## ⚙️ Dependencias principales

- Python 3.11+
- pre-commit
- pytest
- GitHub CLI (opcional, recomendado)
- Rancher Desktop (docker alternative for Mac M1)

---

## Hooks pre-commit incluidos

- `trailing-whitespace` → Remueve espacios innecesarios
- `end-of-file-fixer` → Asegura newline EOF
- `check-yaml` → Valida YAML
- `check-added-large-files` → Evita archivos enormes por accidente
- `black` → Formatea Python bajo PEP8

Instalación:

```bash
pip install pre-commit
pre-commit install
