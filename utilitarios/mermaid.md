# Manual de Diagramas com Mermaid

**Objetivo**

Este manual fornece um guia completo e estruturado sobre como utilizar a linguagem [Mermaid](https://mermaid.js.org/) para criar diagramas em Markdown. Ideal para documentações técnicas, wikis e apresentações.

---
**Introdução**

**Mermaid** é uma linguagem de marcação baseada em texto que permite criar diagramas e visualizações diretamente em arquivos Markdown. É amplamente suportada por ferramentas como:

- GitHub
- GitLab
- Obsidian
- Notion (com plugins)
- MkDocs, Docusaurus, entre outras

---
**Como Usar o Mermaid Live Editor**

1. Acesse: [https://mermaid.live](https://mermaid.live)
2. Escreva o código no painel esquerdo.
3. Visualize o diagrama no painel direito.
4. Exporte como imagem (PNG/SVG) ou compartilhe via link.

---
**Como Usar no README.md**

Para fazer uso dos diagramas desenvolvidos dentro do arquivo README.md, existe algumas maneiras práticas para isso, como:
1. Exportar a imagem do diagrama e inserir no arquivo;
2. Adicionar um bloco de código mermaid no arquivo;
3. Clicar em `Copy Markdown` no Live Editor e colar no arquivo como link.

---

## Fluxograma

### O que é?

Fluxogramas representam o fluxo de processos ou decisões. São úteis para descrever:

- Algoritmos
- Processos de negócio
- Fluxos de usuário
- Lógicas condicionais

### Sintaxe Básica

```mermaid
flowchart TD
  A[Início] --> B{Decisão}
  B -- Sim --> C[Executar ação]
  B -- Não --> D[Encerrar]
  C --> D
```

### Exemplo

[![](https://mermaid.ink/img/pako:eNpVjTFvgzAUhP-K9aZWgogAxuChUgNtlkjtkKnAYAUHowQbGaM0Bf57TaKq7U3vdPfdG-GgKg4Ujmd1OQimDdpnhURWz3kqdNOblvUlct2nacsNapXk1wltHrYK9UJ1XSPrx3t_s5RQOu6WGkdGNPI036P0xr9JPqEs37HOqK78m-wvakIvefMu7Pz_RGhuqdf8yOiRuQemUcp0CQ7UuqmAGj1wB1quW7ZYGBe4ACN4ywug9qyYPhVQyNkyHZMfSrU_mFZDLcDunnvrhq5ihmcNqzX7rXBZcZ2qQRqgfnKbADrCJ9AgilZREpMgwCHGJA4iB65Aw3i1jklI8JrgJIlwODvwdXvqrWKCPSs_8gjxfOzP3-hBdLI?type=png)](https://mermaid.live/edit#pako:eNpVjTFvgzAUhP-K9aZWgogAxuChUgNtlkjtkKnAYAUHowQbGaM0Bf57TaKq7U3vdPfdG-GgKg4Ujmd1OQimDdpnhURWz3kqdNOblvUlct2nacsNapXk1wltHrYK9UJ1XSPrx3t_s5RQOu6WGkdGNPI036P0xr9JPqEs37HOqK78m-wvakIvefMu7Pz_RGhuqdf8yOiRuQemUcp0CQ7UuqmAGj1wB1quW7ZYGBe4ACN4ywug9qyYPhVQyNkyHZMfSrU_mFZDLcDunnvrhq5ihmcNqzX7rXBZcZ2qQRqgfnKbADrCJ9AgilZREpMgwCHGJA4iB65Aw3i1jklI8JrgJIlwODvwdXvqrWKCPSs_8gjxfOzP3-hBdLI)

### Variações

- `flowchart TD` → direção **Top-Down** (de cima para baixo)
- `flowchart LR` → direção **Left to Right** (da esquerda para a direita)
- `flowchart BT` → direção **Bottom to Top**
- `flowchart RL` → direção **Right to Left**

### Simbologia

| Simbolo | Representação | Contexto |
| --- | --- | --- |
| `[]` | Bloco retangular | Processo |
| `{}` | Decisão | Condicional |
| `-->` | Seta de transição | |
| `-- Texto -->` | Seta com rótulo | |

---

## Diagrama de Sequência

### O que é?

Representa a troca de mensagens entre participantes ao longo do tempo. Ideal para:

- APIs
- Comunicação cliente-servidor
- Interações entre sistemas

### Sintaxe Básica

```mermaid
sequenceDiagram
  participant Cliente
  participant Servidor
  Cliente->>Servidor: Requisição HTTP
  Servidor-->>Cliente: Resposta com dados
```

### Exemplo

[![](https://mermaid.ink/img/pako:eNptkM1OwzAMgF8l85W0SqK1WXMYQnBgPALqJWq9tqJJRtYIRtV3J80Yp_nkn--zJc_QuBZBwRk_A9oGXwbdeW1qS2I8jUOD2X7_8OZ6q8grjqMja05J776I9kguLjzeha9Yo-2KkB61Jwb_0HWWRTRLTlw8XG1KDslIdNQ29_EDOSKOpPOopw1Q6PzQgpp8QAoGvdFrCfMq1zD1aLAGFdNW-48aartE56Ttu3PmpnkXuh7UUY_nWIVTq6fbK_4RtC36ZxfsBGrL0wpQM3yDEiXPC1kVglWCbaWQFC6gyjKXUvCdFDtZcF7xhcJPusny2GExRMmkZKLgyy98J3do?type=png)](https://mermaid.live/edit#pako:eNptkM1OwzAMgF8l85W0SqK1WXMYQnBgPALqJWq9tqJJRtYIRtV3J80Yp_nkn--zJc_QuBZBwRk_A9oGXwbdeW1qS2I8jUOD2X7_8OZ6q8grjqMja05J776I9kguLjzeha9Yo-2KkB61Jwb_0HWWRTRLTlw8XG1KDslIdNQ29_EDOSKOpPOopw1Q6PzQgpp8QAoGvdFrCfMq1zD1aLAGFdNW-48aartE56Ttu3PmpnkXuh7UUY_nWIVTq6fbK_4RtC36ZxfsBGrL0wpQM3yDEiXPC1kVglWCbaWQFC6gyjKXUvCdFDtZcF7xhcJPusny2GExRMmkZKLgyy98J3do)

### Simbologia

| Simbolo | Representação | 
| --- | --- | 
| `participant` | Define um ator | 
| `->>` | Mensagem síncrona | 
| `-->>` | Mensagem assíncrona | 
| `+` | Abre uma caixa de processo (request) | |
| `-` | Fecha uma caixa de processo (response) | |
| `Note right of` | Adiciona anotações | 

---

## Diagrama de Estado

### O que é?

Representa os estados possíveis de um sistema e suas transições. Útil para:

- Máquinas de estado
- Ciclos de vida de objetos
- Fluxos de interface

### Sintaxe 

```mermaid
stateDiagram-v2
  [*] --> Aberto
  Aberto --> EmProgresso : iniciar
  EmProgresso --> Concluido : finalizar
  Concluido --> [*]
```

### Exemplo

[![](https://mermaid.ink/img/pako:eNpdjzFvwyAQhf-KdWNlWzYBQxi6JGumbC0dUKC2VQMRxlFay_-9BCtplZve--7enW6Gk1MaOIxBBr3vZeulKS5I2CzW-8tHVhSv2TH0w7CiJBOMzWd0cJfetitd9XP8H915OXYrTfK-FHJofa-ABz_pHIz2Rt4szLdhAaHTRgvgUSrpvwQIu8TMWdo358w95t3UdsA_5TBGN53V33uPEW2V9js32QCcbNIK4DNco2OopKjGFBFEGN40OXwDx6ysGcWU1JRstw3BSw4_6WZVMkqqWKipKK0QqZdf4GZl0A?type=png)](https://mermaid.live/edit#pako:eNpdjzFvwyAQhf-KdWNlWzYBQxi6JGumbC0dUKC2VQMRxlFay_-9BCtplZve--7enW6Gk1MaOIxBBr3vZeulKS5I2CzW-8tHVhSv2TH0w7CiJBOMzWd0cJfetitd9XP8H915OXYrTfK-FHJofa-ABz_pHIz2Rt4szLdhAaHTRgvgUSrpvwQIu8TMWdo358w95t3UdsA_5TBGN53V33uPEW2V9js32QCcbNIK4DNco2OopKjGFBFEGN40OXwDx6ysGcWU1JRstw3BSw4_6WZVMkqqWKipKK0QqZdf4GZl0A)

### Simbologia

| Simbolo | Representação 
| --- | --- |
| `[*]` | Estado inicial ou final | 
| `-->` | Transição | 
| `: evento` | Evento que dispara a transição | 

---

## Diagrama de Gantt

### O que é?

Representa cronogramas de projetos com tarefas, datas e dependências.

### Sintaxe Básica

```mermaid
gantt
  title Cronograma do Projeto
  dateFormat  YYYY-MM-DD
  section Planejamento
  Análise de Requisitos     :a1, 2025-07-01, 5d
  Design da Solução         :a2, after a1, 4d
  section Execução
  Desenvolvimento           :b1, after a2, 10d
  Testes                    :b2, after b1, 5d
```

### Exemplo

[![](https://mermaid.ink/img/pako:eNpdkMtuwjAQRX9lNOsE-ZEX3qGidsWq3bTKZoRNiCA2Mo7UFvHvtUkoaq8s2TN3jq_sC26dNqiwIxtCayEq9OFoYAUvqQXrnjpPw2RpCubZ-YECwHtUvtnk6_Xknc029M7C67RPzRUEOh_gIUU8A8F4kTMeVwaS6XnUurA3_gEo2oVYEwdIiP4bM49PzbfE9DaZc8w9gotEczHT9D8EFIhCY4ad7zWq4EeT4WDiE1OJl4S1GJnBtKjiUZM_tNjaa2ROZD-cG-6Yd2O3R7Wj4zlW4yn91vx9vyPGauOf3GgDqqq8XYHqgp-oGr4QxXJZSSmrohFlk-EXKinqBZcVF1yWy-jz6prh9y2ULZq6ZFGiYnXNRCmvP79qhDc?type=png)](https://mermaid.live/edit#pako:eNpdkMtuwjAQRX9lNOsE-ZEX3qGidsWq3bTKZoRNiCA2Mo7UFvHvtUkoaq8s2TN3jq_sC26dNqiwIxtCayEq9OFoYAUvqQXrnjpPw2RpCubZ-YECwHtUvtnk6_Xknc029M7C67RPzRUEOh_gIUU8A8F4kTMeVwaS6XnUurA3_gEo2oVYEwdIiP4bM49PzbfE9DaZc8w9gotEczHT9D8EFIhCY4ad7zWq4EeT4WDiE1OJl4S1GJnBtKjiUZM_tNjaa2ROZD-cG-6Yd2O3R7Wj4zlW4yn91vx9vyPGauOf3GgDqqq8XYHqgp-oGr4QxXJZSSmrohFlk-EXKinqBZcVF1yWy-jz6prh9y2ULZq6ZFGiYnXNRCmvP79qhDc)

### Simbologia

| Símbolo         | Representação             |
|-----------------|---------------------------|
| `section`       | Agrupamento de tarefas    |
| `:id, data, duração` | Define tarefa         |
| `after id`      | Define dependência        |

---

## Diagrama de Classes

### O que é?

Representa a estrutura de classes em sistemas orientados a objetos.

### Sintaxe Básica

```mermaid
classDiagram
  class Pessoa {
    +String nome
    +int idade
    +falar()
  }
  class Aluno
  Pessoa <|-- Aluno
```

### Exemplo

[![](https://mermaid.ink/img/pako:eNptUdFOgzAU_ZXmPmlkCwNGsfHFbC7xwSffFhJzgcoaaDvbkunm_l1Awbl5n-45t-f09PYAuS44MMhrtHYpsDQoU0XauldCYk3uPicTsmzy6pJdCbu5ZNc8M_iHZuRGKEew5Of0szNClaTkquDmdNhJ7BPKtr26PhtIdHwg-9h9vMM3QUbTjGO10LU248DuhByELXxrMK8GfDz16x42-k267Fbs-aNace5GOkf1gO5ffb-C30CZ1jUR9mUn6mIkTaNGLXhQGlEAc6bhHkhuJHYQeo8U3IZLngJr2wJNlUKqOs0W1VprOciMbsoNsFesbYuabdHu6edHxyP9ohe6UQ4Ypb0FsAO8Awv82TQJw_ltSGkShXEce_ABLEqms4RGNImDxA_oLDp6sO8v9acJnfttBbFPqR_Mj1-rQa8c?type=png)](https://mermaid.live/edit#pako:eNptUdFOgzAU_ZXmPmlkCwNGsfHFbC7xwSffFhJzgcoaaDvbkunm_l1Awbl5n-45t-f09PYAuS44MMhrtHYpsDQoU0XauldCYk3uPicTsmzy6pJdCbu5ZNc8M_iHZuRGKEew5Of0szNClaTkquDmdNhJ7BPKtr26PhtIdHwg-9h9vMM3QUbTjGO10LU248DuhByELXxrMK8GfDz16x42-k267Fbs-aNace5GOkf1gO5ffb-C30CZ1jUR9mUn6mIkTaNGLXhQGlEAc6bhHkhuJHYQeo8U3IZLngJr2wJNlUKqOs0W1VprOciMbsoNsFesbYuabdHu6edHxyP9ohe6UQ4Ypb0FsAO8Awv82TQJw_ltSGkShXEce_ABLEqms4RGNImDxA_oLDp6sO8v9acJnfttBbFPqR_Mj1-rQa8c)

### Simbologia

| Símbolo     | Representação                  |
|-------------|--------------------------------|
| `class`     | Define uma classe              |
| `+`         | Público                        |
| `-`         | Privado                        |
| `<|--`      | Herança                        |

---

## Diagrama ER (Entidade-Relacionamento)

### O que é?

Representa entidades, atributos e relacionamentos em bancos de dados.

### Sintaxe Básica

```mermaid
erDiagram
  CLIENTE ||--o{ PEDIDO : faz
  PEDIDO ||--|{ ITEM : contém
  CLIENTE {
    string nome
    string email
  }
```

### Exemplo 

[![](https://mermaid.ink/img/pako:eNp1kdFugjAUhl-lOddAEIVC7wyQhWSOBdHEhZsOqpIBNRXMNuDdV1S26bJzd5rv__6mbSHlGQMCTHg53QlaJhWS466WcbjwI9R3mta1yPMfg7UfbdS550X-cokI2tPjHdt1qspbFEaeXAg6FDRl_zDB0zoMXF9SCRQ5fS0Y2nKRwIX-03ZnFixl-Wl0j64B6n6glJ-YuCKXs9-AGsT-QlJ5lRZNNqqeo9BbubHqzmP_IYw2Y-R6frZWNc2rW_7mfqM5AS4yJlgmOxIABXYiz4DUomEKlEyUdFihHUwJ1HtWsgSGWEbF2_ASvcwcaPXCeTnGBG92eyBbWhzl1hwyWrPrv30jrJKtLm-qGojtnBVAWngHYui6hh3HNnR7hi3DmFoKfACZ2drExjNsTrDpOJY57RX4PJfqmo1NXY5h6Rjrhtl_AS0SplE?type=png)](https://mermaid.live/edit#pako:eNp1kdFugjAUhl-lOddAEIVC7wyQhWSOBdHEhZsOqpIBNRXMNuDdV1S26bJzd5rv__6mbSHlGQMCTHg53QlaJhWS466WcbjwI9R3mta1yPMfg7UfbdS550X-cokI2tPjHdt1qspbFEaeXAg6FDRl_zDB0zoMXF9SCRQ5fS0Y2nKRwIX-03ZnFixl-Wl0j64B6n6glJ-YuCKXs9-AGsT-QlJ5lRZNNqqeo9BbubHqzmP_IYw2Y-R6frZWNc2rW_7mfqM5AS4yJlgmOxIABXYiz4DUomEKlEyUdFihHUwJ1HtWsgSGWEbF2_ASvcwcaPXCeTnGBG92eyBbWhzl1hwyWrPrv30jrJKtLm-qGojtnBVAWngHYui6hh3HNnR7hi3DmFoKfACZ2drExjNsTrDpOJY57RX4PJfqmo1NXY5h6Rjrhtl_AS0SplE)

### Simbologia

| Símbolo | Representação                  |
|---------|--------------------------------|
| `||--o{` | Um para muitos                |
| `||--||` | Um para um                   |
| `o{--o{` | Muitos para muitos           |

---

## Diagrama de Fluxo de Usuário

### O que é?

Representa o caminho que um usuário percorre em um sistema.

### Sintaxe Básica

```mermaid
graph TD
  Start --> Login
  Login --> Dashboard
  Dashboard --> Logout
```

### Exemplo

[![](https://mermaid.ink/img/pako:eNplTztvwjAQ_iunmyNk541XkJgydatYLHxNXIgdObYoRfnvdQJRqXrT3ffU3fFkFaHATxucodvRQByv_YWgucHVurM2LSj5ZEY6eW0NHCx4u9APHKCRZwJPUkAhoKEVjsIwjF5qNwrIXpn9wy-Az2gCO-n_dXS2f01S9mrWrD8tb9ov5LMCE2ydVii8C5RgT66X84n32XBE31HMRRFXJeMLeDRT9AzSvFvbrzZnQ9uh-JCXMV5hUNLTXsvWyV8JGUVuZ4PxKDjjSwaKO36hqPkmzbfbouZ5VrGsjOQtiiq-4RGvS56xKs_KdErwe2llm7oqWJy0ZFXF0mL6AQvIeyc?type=png)](https://mermaid.live/edit#pako:eNplTztvwjAQ_iunmyNk541XkJgydatYLHxNXIgdObYoRfnvdQJRqXrT3ffU3fFkFaHATxucodvRQByv_YWgucHVurM2LSj5ZEY6eW0NHCx4u9APHKCRZwJPUkAhoKEVjsIwjF5qNwrIXpn9wy-Az2gCO-n_dXS2f01S9mrWrD8tb9ov5LMCE2ydVii8C5RgT66X84n32XBE31HMRRFXJeMLeDRT9AzSvFvbrzZnQ9uh-JCXMV5hUNLTXsvWyV8JGUVuZ4PxKDjjSwaKO36hqPkmzbfbouZ5VrGsjOQtiiq-4RGvS56xKs_KdErwe2llm7oqWJy0ZFXF0mL6AQvIeyc)

### Simbologia

| Símbolo | Representação         |
|---------|-----------------------|
| `-->`   | Transição entre telas |
| `[]`    | Etapas ou ações       |

---
## Diagrama de Git

### O que é?

Visualiza branches e merges em repositórios Git.

### Sintaxe Básica

```mermaid
gitGraph
  commit
  branch develop
  checkout develop
  commit
  checkout main
  merge develop
```

### Exemplo

[![](https://mermaid.ink/img/pako:eNqFTctuwyAQ_JVoz5ZFFhPbXFup_xBxoWYLVgJYFKK2lv-9NH1JrarOaWZ2ZnaFKRoCCXbOd0kvToVdxRS9n_Nvfp90mNzO0IXOcfm4O5pOseQf7h8LX2mv5_BueUqW_mtDAzbNBmROhRqonTpQJaxvKQXZkScFslKj00mBClvtLDocY_SftRSLdSAf9PmxqrIYnel21jbp7wgFQ-kmlpBBciauGyBXeKrygC3vxl7sO2QDR2zgGSQib3EUOPScjUPHcWvg5fqUtUMvWAUeWN8zFPvtFT4Yct4?type=png)](https://mermaid.live/edit#pako:eNqFTctuwyAQ_JVoz5ZFFhPbXFup_xBxoWYLVgJYFKK2lv-9NH1JrarOaWZ2ZnaFKRoCCXbOd0kvToVdxRS9n_Nvfp90mNzO0IXOcfm4O5pOseQf7h8LX2mv5_BueUqW_mtDAzbNBmROhRqonTpQJaxvKQXZkScFslKj00mBClvtLDocY_SftRSLdSAf9PmxqrIYnel21jbp7wgFQ-kmlpBBciauGyBXeKrygC3vxl7sO2QDR2zgGSQib3EUOPScjUPHcWvg5fqUtUMvWAUeWN8zFPvtFT4Yct4)

### Simbologia

| Símbolo     | Representação         |
|-------------|-----------------------|
| `commit`    | Confirmação de código |
| `branch`    | Criação de branch     |
| `merge`     | Mesclagem de branches |

---

## Diagrama de Matriz

### O que é?

Representa relações cruzadas entre elementos.

### Sintaxe Básica

```mermaid
quadrantChart
    title Reach and engagement of campaigns
    x-axis Low Reach --> High Reach
    y-axis Low Engagement --> High Engagement
    quadrant-1 We should expand
    quadrant-2 Need to promote
    quadrant-3 Re-evaluate
    quadrant-4 May be improved
    Campaign A: [0.3, 0.6]
    Campaign B: [0.45, 0.23]
    Campaign C: [0.57, 0.69]
    Campaign D: [0.78, 0.34]
    Campaign E: [0.40, 0.34]
    Campaign F: [0.35, 0.78]
```

### Exemplo

[![](https://mermaid.ink/img/pako:eNptkE9PwzAMxb-K5XNb9d-akgMSDBAH4MAFCcrBrKatWJORpbAx7buTtRtDhZzi_N6zX7zBmS4ZJb53VBpSdlqTsYUCd2xj5wz3TLMaSJXAqqKKW1YW9CvMqF1QU6nlIF75tGqWcKM_9w7fP4XrpqqHchCtj6LLY7Mf5fFtkB8y-RE8MCxr3c1ditXChRkJYrhjLsFqWBjdassjnrgUPn_QvKM_LIVbWsMLQ9M68wfve0_3_4MzCU9hkHgQBtnziJ33LJ3sYJyM6bSnE9FbT8b0oqci39EkHdPLoXP4P70aMvVzRf6MHlamKVFa07GHLZuWdiVudr4Cbe22WqB015LMW4GF2jqPW-Sj1u3BZnRX1Shfab50Vbco3a4uGqoMHSWsSjZT3SmLMkr6Fig3uEKZRHGQ5SIVeRSJKM4yD9co0zyIfj9G2dbDr35oGORiEroTZ6EQYTxJtt8v98WO?type=png)](https://mermaid.live/edit#pako:eNptkE9PwzAMxb-K5XNb9d-akgMSDBAH4MAFCcrBrKatWJORpbAx7buTtRtDhZzi_N6zX7zBmS4ZJb53VBpSdlqTsYUCd2xj5wz3TLMaSJXAqqKKW1YW9CvMqF1QU6nlIF75tGqWcKM_9w7fP4XrpqqHchCtj6LLY7Mf5fFtkB8y-RE8MCxr3c1ditXChRkJYrhjLsFqWBjdassjnrgUPn_QvKM_LIVbWsMLQ9M68wfve0_3_4MzCU9hkHgQBtnziJ33LJ3sYJyM6bSnE9FbT8b0oqci39EkHdPLoXP4P70aMvVzRf6MHlamKVFa07GHLZuWdiVudr4Cbe22WqB015LMW4GF2jqPW-Sj1u3BZnRX1Shfab50Vbco3a4uGqoMHSWsSjZT3SmLMkr6Fig3uEKZRHGQ5SIVeRSJKM4yD9co0zyIfj9G2dbDr35oGORiEroTZ6EQYTxJtt8v98WO)

### Simbologia

| Símbolo         | Representação         |
|-----------------|-----------------------|
| `x-axis`        | Eixo horizontal       |
| `y-axis`        | Eixo vertical         |
| `\"label\": [x, y]` | Ponto no gráfico  |

---
## Dicas de Implementação

- Certifique-se de que o arquivo tenha a extensão `.md`.
- Visualize o diagrama diretamente na interface do GitHub.
- Evite usar muitos diagramas pesados em um único arquivo para não comprometer a performance.
- Para documentação extensa, considere separar os diagramas em arquivos `.md` específicos.