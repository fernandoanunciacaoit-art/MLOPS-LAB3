# LAB3 — Automação MLOps com CI/CD e GitHub Actions

Este laboratório demonstra, de forma prática, como automatizar etapas de um pipeline MLOps utilizando GitHub Actions.

O foco principal é aplicar o conceito de Continuous Integration (CI) ao ciclo de Machine Learning, fazendo com que alterações no repositório iniciem automaticamente a preparação do ambiente, o treinamento, a avaliação do modelo e a aplicação de um Quality Gate.

## Objetivo

Demonstrar como mudanças no código podem disparar automaticamente um pipeline de Machine Learning com critérios de aprovação e bloqueio.

## Fluxo do laboratório

Código
→ Commit / Push
→ GitHub Actions
→ Runner Ubuntu
→ Setup Python
→ Instalação de dependências
→ Treinamento
→ Avaliação
→ Quality Gate
→ PASS / FAIL

## Tecnologias utilizadas

- Python
- Scikit-learn
- Random Forest
- GitHub
- GitHub Actions

## Conceitos demonstrados

- Continuous Integration (CI);
- automação de pipelines;
- execução automática de treinamento;
- avaliação automática de modelos;
- Quality Gate;
- aprovação e bloqueio com base em métricas;
- uso de código de saída para controle do pipeline;
- reprodutibilidade do ambiente com `requirements.txt`;
- execução automatizada em runner Ubuntu.

## Modelo utilizado

Neste laboratório utilizamos um modelo de Machine Learning baseado em Random Forest para classificação.

O modelo é treinado automaticamente pelo pipeline e avaliado utilizando as métricas:

- Accuracy
- F1-Score

## Quality Gate

O pipeline utiliza critérios mínimos de qualidade para decidir se a execução deve ser aprovada ou bloqueada.

Exemplo:

Accuracy do modelo: 0.958

Critério:

MIN_ACCURACY = 0.93

Resultado:

QUALITY GATE: PASS

Ao alterar o critério para:

MIN_ACCURACY = 0.99

o mesmo modelo deixa de atender à política definida:

QUALITY GATE: FAIL

## Arquitetura do LAB

DESENVOLVEDOR
      ↓
ALTERAÇÃO NO CÓDIGO
      ↓
COMMIT / PUSH
      ↓
GITHUB ACTIONS
      ↓
RUNNER UBUNTU
      ↓
SETUP PYTHON
      ↓
INSTALL DEPENDENCIES
      ↓
TREINAMENTO
      ↓
AVALIAÇÃO
      ↓
QUALITY GATE
     / \
    /   \
 PASS   FAIL
  ↓       ↓
CONTINUA BLOQUEIA

## Resultado esperado

Ao final do laboratório, o participante deverá compreender como um evento no repositório pode disparar automaticamente um pipeline de Machine Learning, executar treinamento e avaliação e aplicar critérios de qualidade para aprovar ou bloquear a execução.

## Importante

Neste laboratório implementamos principalmente o conceito de Continuous Integration (CI).

Não realizamos um deploy real do modelo em produção. Portanto, o componente de Continuous Delivery/Deployment (CD) é apresentado como parte do contexto de MLOps, mas não é implementado neste laboratório.

Laboratório desenvolvido exclusivamente para fins educacionais.
