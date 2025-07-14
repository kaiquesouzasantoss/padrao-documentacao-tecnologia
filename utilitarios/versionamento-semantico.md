# Padrões de Vesionamento Semântico

O versionamento semântico é uma prática essencial no desenvolvimento de software moderno. Ele estabelece uma convenção clara e padronizada para nomear versões de sistemas, bibliotecas e APIs, facilitando a comunicação entre desenvolvedores, equipes e usuários finais.

---
**Por que o Versionamento Semântico é Importante?**

- **Clareza na Evolução do Projeto**: Permite entender rapidamente se uma nova versão contém correções, novas funcionalidades ou mudanças incompatíveis.
- **Facilita Integrações**: Equipes que dependem de bibliotecas externas podem avaliar com segurança se uma atualização afetará seus sistemas.
- **Evita Quebras Inesperadas**: Ao seguir a convenção, mudanças que quebram compatibilidade são claramente sinalizadas.
- **Melhora a Manutenção**: Ajuda na rastreabilidade de bugs e regressões ao associar versões a mudanças específicas.

---
**Termos Fundamentais**

| Termo | Definição | Exemplo | Importância |
| --- | --- | --- | --- |
| Commit | Um *commit* é o registro de uma alteração no código-fonte. Ele representa um ponto específico na linha do tempo do projeto. | `feat(auth): adicionar endpoint de login` | Permite rastrear o histórico de mudanças e entender o motivo de cada modificação. |
| Branch | Uma *branch* (ramificação) é uma linha paralela de desenvolvimento. Permite trabalhar em funcionalidades ou correções isoladamente, sem afetar o código principal. | `feature/123-login-usuario` | Facilita o trabalho colaborativo e a organização do fluxo de desenvolvimento. |
| Issue | Uma *issue* é um item de rastreamento que representa uma tarefa, bug ou sugestão. É usada para planejar e documentar o trabalho a ser feito. | `#456 - Corrigir erro no endpoint de autenticação` | Centraliza a comunicação sobre problemas e funcionalidades, promovendo transparência e organização. |

---
**Nomenclatura de Versão**

O padrão segue o formato: `MAJOR`.`MINOR`.`PATCH` -> sistema (`2`.`1`.`4`)

| Formato | Descrição |
| --- | --- |
| MAJOR | Mudanças incompatíveis com versões anteriores |
| MINOR | Novas funcionalidades compatíveis |
| PATCH |Correções de bugs compatíveis |

---
## Commit
### Estrutura

```txt
<tipo>[escopo opcional]: <descrição curta>

[corpo opcional]
[rodapé(s) opcional(is)]
```

---
### Tipos

| Tipo     | Descrição                                              |
|----------|--------------------------------------------------------|
| feat     | Nova funcionalidade                                    |
| fix      | Correção de bug                                        |
| docs     | Alterações na documentação                             |
| style    | Formatação, espaços, etc (sem impacto funcional)       |
| refactor | Refatoração sem mudança de comportamento               |
| perf     | Melhorias de performance                               |
| test     | Adição ou ajuste de testes                             |
| chore    | Tarefas de manutenção (build, configs)                 |
| build    | Alterações em dependências e build                     |
| env      | Configurações de ambiente, CI/CD                       |

---
### Exemplos

- feat(auth): adicionar endpoint de login
- fix(api): corrigir erro no endpoint de consulta
- docs: atualizar README com instruções de deploy

---
### Boas Práticas

- Título no imperativo, com até 72 caracteres.
- Corpo opcional: use para explicar o "porquê" da mudança.
- Rodapé: use Closes #123 ou Refs #456 para vincular issues.

Referência: https://www.conventionalcommits.org/

---
## Branch
### Estrutura

```txt
<tipo>/<id-da-issue>-<descricao-curta>
```

---
### Tipos

| Tipo      | Uso                                 |
|-----------|-------------------------------------|
| feature   | Novas funcionalidades               |
| bugfix    | Correções de bugs                   |
| hotfix    | Correções urgentes em produção      |
| release   | Preparação para releases            |

---
### Exemplos

- feature/123-login-usuario
- bugfix/456-corrigir-endpoint-consulta
- hotfix/789-corrigir-falha-producao

**Dica**: Use nomes descritivos e inclua o número da issue sempre que possível.

---
## Issue e Tarefa
### Template de Issue

```txt
Título da Issue
> Breve descrição do problema ou funcionalidade.

Descrição:
> Detalhe o problema ou a funcionalidade.

Passos para Reproduzir (se aplicável):
1. Passo 1
2. Passo 2

Comportamento Esperado:
Descreva o comportamento correto.

Comportamento Atual:
Descreva o que está acontecendo.

Ambiente:
- SO:
- Versão da aplicação:

Anexos:
(Imagens, logs, etc.)

Referências:
- Issue relacionada: #123

```

---
### Template de Tarefa

```txt
Tarefa: [Descrição da Tarefa]

Objetivo:
> Descrever brevemente o objetivo da tarefa.

Checklist:
- [ ] Analisar requisitos
- [ ] Desenvolver funcionalidade
- [ ] Testar
- [ ] Atualizar documentação
- [ ] Revisão de código

Notas Adicionais:
> Observações, dependências ou links úteis.
```