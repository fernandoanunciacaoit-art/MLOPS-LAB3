# LAB3 — Automação MLOps com CI/CD e GitHub Actions

Este laboratório demonstra, de forma prática, como automatizar etapas de um pipeline MLOps utilizando GitHub Actions.

O foco principal é aplicar Continuous Integration (CI) ao ciclo de Machine Learning, executando automaticamente treinamento, avaliação e Quality Gate.

## Objetivo

Demonstrar como um pipeline de Machine Learning pode ser disparado automaticamente por alterações no repositório ou manualmente pelo GitHub Actions.

## Fluxo

Código  
→ Commit / Push  
→ GitHub Actions  
→ Instalação de dependências  
→ Treinamento  
→ Avaliação  
→ Quality Gate  
→ PASS / FAIL

## Tecnologias

- Python
- Scikit-learn
- Random Forest
- GitHub
- GitHub Actions

## Conceitos demonstrados

- Continuous Integration (CI)
- automação de pipeline
- treinamento automático
- avaliação automática
- Quality Gate
- aprovação e bloqueio por métricas
- execução automática por `push`
- execução manual com `workflow_dispatch`

## Quality Gate

O pipeline utiliza critérios mínimos de qualidade para decidir se a execução será aprovada ou bloqueada.

Exemplo:

```text
MIN_ACCURACY = 0.93
Accuracy = 0.958

QUALITY GATE: PASS
