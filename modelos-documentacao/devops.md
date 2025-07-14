<h1 align=center>Documentação Técnica de Projeto DevOps / CI-CD</h1>

## Índice
- [Visão Geral do Projeto](#visão-geral-do-projeto)
- [Escopo da Automação](#escopo-da-automação)
- [Pipeline de CI/CD](#pipeline-de-cicd)
- [Infraestrutura como Código (IaC)](#infraestrutura-como-código-iac)
- [Ambientes](#ambientes)
- [Estratégia de Deploy](#estratégia-de-deploy)
- [Automação de Tarefas](#automação-de-tarefas)
- [Segurança e Conformidade](#segurança-e-conformidade)
- [Monitoramento e Observabilidade](#monitoramento-e-observabilidade)
- [Estratégia de Rollback](#estratégia-de-rollback)
- [Ferramentas Utilizadas](#ferramentas-utilizadas)
- [Lições Aprendidas](#lições-aprendidas)
- [Anexos](#anexos)

---
## Visão Geral do Projeto
**Objetivo:** Apresentar uma visão macro da estratégia DevOps e CI/CD adotada no projeto.

**O que deve conter:**
- Nome do projeto
- Equipes envolvidas (Dev, QA, Ops, Segurança)
- Objetivo principal da automação de entrega
- Justificativa da adoção de práticas DevOps

**Perguntas orientadoras:**
- Qual problema estamos resolvendo com DevOps?
- Quais áreas serão beneficiadas com a automação?

---
## Escopo da Automação

**Objetivo:** Delimitar claramente o que será automatizado no ciclo de vida da aplicação.

**O que deve conter:**
- Etapas automatizadas (build, test, deploy, monitoramento)
- Restrições técnicas ou operacionais
- Processos manuais que permanecerão

**Perguntas orientadoras:**
- Quais etapas do ciclo de vida estão cobertas?
- Existem limitações de ferramentas ou ambientes?

---
## Pipeline de CI/CD

**Objetivo:** Descrever o fluxo de integração e entrega contínua.

**O que deve conter:**
- Diagrama do pipeline
- Etapas do pipeline (build, test, approval, deploy)
- Gatilhos (push, merge, agendado)
- Estratégia de versionamento

**Perguntas orientadoras:**
- Como o código é validado e entregue?
- Existem etapas manuais no pipeline?

---
## Infraestrutura como Código (IaC)

**Objetivo:** Documentar a infraestrutura provisionada via código.

**O que deve conter:**
- Ferramentas utilizadas (Terraform, Ansible, Pulumi, etc.)
- Estrutura dos arquivos
- Ambientes provisionados
- Estratégia de versionamento da infraestrutura

**Perguntas orientadoras:**
- Como a infraestrutura é criada e atualizada?
- Onde o código de infraestrutura está armazenado?

---
## Ambientes

**Objetivo:** Descrever os ambientes utilizados no ciclo de vida da aplicação.

**O que deve conter:**
- Ambientes existentes (dev, staging, prod, etc.)
- Estratégia de isolamento
- Configurações específicas por ambiente
- Estratégia de gerenciamento de segredos

**Perguntas orientadoras:**
- Como os ambientes são separados?
- Como são gerenciadas as variáveis sensíveis?

---
## Estratégia de Deploy

**Objetivo:** Documentar como as entregas são realizadas em produção.

**O que deve conter:**
- Tipo de deploy (rolling, blue/green, canary)
- Ferramentas utilizadas
- Janelas de deploy
- Aprovações manuais (se houver)

---
## Automação de Tarefas

**Objetivo:** Detalhar tarefas operacionais automatizadas além do pipeline.

**O que deve conter:**
- Scripts de manutenção, limpeza, backup
- Agendamentos (cron jobs, workflows)
- Ferramentas utilizadas (ex: GitHub Actions, Jenkins, ArgoCD)

**Perguntas orientadoras:**
- Quais tarefas foram automatizadas?
- Como são executadas e monitoradas?

---
## Segurança e Conformidade

**Objetivo:** Garantir que o processo esteja em conformidade com políticas de segurança.

**O que deve conter:**
- Scans de vulnerabilidade (SAST, DAST, SCA)
- Gestão de segredos (Vault, AWS Secrets Manager, etc.)
- Controle de acesso ao pipeline
- Logs e auditoria

**Perguntas orientadoras:**
- Como protegemos o pipeline e os ambientes?
- Existem políticas de conformidade aplicadas?

---
## Monitoramento e Observabilidade

**Objetivo:** Definir como o sistema e o pipeline são monitorados.

**O que deve conter:**
- Ferramentas utilizadas (Prometheus, Grafana, ELK, Datadog, etc.)
- Métricas monitoradas
- Alertas e notificações
- Dashboards

**Perguntas orientadoras:**
- Como detectamos falhas em tempo real?
- Quais indicadores são acompanhados?

---
## Estratégia de Rollback

**Objetivo:** Descrever como reverter uma entrega em caso de falha.

**O que deve conter:**
- Estratégia de rollback (manual, automático, blue/green, canary)
- Tempo estimado de recuperação
- Ferramentas envolvidas

**Perguntas orientadoras:**
- Como desfazemos uma entrega com problema?
- Existe automação para rollback?

---
## Ferramentas Utilizadas

### Tecnologias Principais

| Tecnologia       | Versão | Finalidade                         | Documentação                          |
|------------------|--------|------------------------------------|----------------------------------------|
| Git              | 2.x    | Controle de versão                 | https://git-scm.com/doc                |
| Docker           | 20.x   | Containerização                    | https://docs.docker.com/               |
| Kubernetes       | 1.x    | Orquestração de containers         | https://kubernetes.io/docs/            |

### Ferramentas de Desenvolvimento

| Ferramenta        | Versão | Finalidade                         | Documentação                          |
|-------------------|--------|------------------------------------|----------------------------------------|
| GitHub Actions    | N/A    | CI/CD                              | https://docs.github.com/actions        |
| Terraform         | 1.x    | Infraestrutura como código         | https://developer.hashicorp.com/terraform |
| Prometheus        | 2.x    | Coleta de métricas                 | https://prometheus.io/docs/            |
| Grafana           | 9.x    | Visualização de métricas           | https://grafana.com/docs/              |

### Outras Dependências

| Dependência       | Versão | Finalidade                         | Documentação                          |
|-------------------|--------|------------------------------------|----------------------------------------|
| Vault             | 1.x    | Gestão de segredos                 | https://developer.hashicorp.com/vault |
| SonarQube         | 9.x    | Análise estática de código         | https://docs.sonarsource.com/          |

---

**Objetivo:** Listar as ferramentas adotadas no processo DevOps.

**O que deve conter:**
- Ferramentas de CI/CD
- Ferramentas de IaC
- Ferramentas de monitoramento
- Ferramentas de segurança
- Justificativa da escolha

**Perguntas orientadoras:**
- Quais ferramentas compõem o ecossistema DevOps?
- Por que essas ferramentas foram escolhidas?

---
## Lições Aprendidas

**Objetivo:** Registrar aprendizados para projetos futuros.

**O que deve conter:**
- O que funcionou bem
- O que poderia ter sido melhor
- Recomendações para próximos projetos

**Perguntas orientadoras:**
- O que aprendemos com este projeto?
- Como podemos melhorar nos próximos?

---
## Anexos

**Objetivo:** Incluir materiais complementares.

**O que deve conter:**
- Diagramas
- Links úteis
- Documentos de apoio

---
## Contribuição

```
$ git clone https://github.com/xxx.git 
```
