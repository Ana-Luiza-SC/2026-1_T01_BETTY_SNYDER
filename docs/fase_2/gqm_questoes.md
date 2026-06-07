# Questões GQM

Esta seção apresenta as questões derivadas de cada objetivo de medição definido na etapa anterior, seguindo a metodologia *Goal-Question-Metric* (GQM) conforme [Ramos (2025)](#ref01) e [Basili, Caldiera e Rombach (2002)](#ref02). Cada questão foi elaborada a partir das necessidades reais de uso do [No Fluxo UnB](#ref03), considerando seus módulos funcionais descritos em [Descrição do Software](../fase_1_v2/descricao.md).

---

## Questões do Objetivo 1: Avaliação de Usabilidade

As questões a seguir derivam do [Objetivo GQM 1 — Usabilidade](./gqm_objetivo.md#objetivo1) e buscam operacionalizar a avaliação das subcaracterísticas de **Reconhecimento da Adequação**, **Capacidade de Aprendizado**, **Proteção contra Erros do Usuário** e **Acessibilidade**, conforme definidas em [Tabela 2 — Usabilidade](../fase_1_v2/caracteristicas.md#usabilidade).

### Subcaracterística: Reconhecimento da Adequação

<p align="center">Tabela 1 – Questões relativas à subcaracterística Reconhecimento da Adequação.</p>

| ID | Questão |
| :---: | :--- |
| **Q1.1** | Em que medida a tela inicial da plataforma comunica, de forma imediata e sem ambiguidade, o propósito central do sistema de planejamento de fluxo acadêmico para o estudante da UnB? |
| **Q1.2** | Os elementos visuais da interface inicial (títulos, ícones, chamadas para ação) são suficientes para que o usuário identifique, sem auxílio externo, quais funcionalidades estão disponíveis? |

<p align="center">Fonte: Do autor (2026).</p>

---

### Subcaracterística: Capacidade de Aprendizado

<p align="center">Tabela 2 – Questões relativas à subcaracterística Capacidade de Aprendizado.</p>

| ID | Questão |
| :---: | :--- |
| **Q1.3** | Quanto tempo um estudante da UnB leva, no primeiro acesso e sem suporte externo, para concluir com sucesso o fluxo completo de importação do histórico escolar em PDF e visualizar o grafo resultante do seu fluxograma? |
| **Q1.4** | A interface do módulo **Meu Fluxograma** fornece pistas visuais suficientes (legendas, tooltips, cores topológicas) para que o usuário compreenda, de forma autônoma, a estrutura de pré-requisitos exibida no grafo? |
| **Q1.5** | Após interagir com o **Assistente Darcy AI** pela primeira vez, o usuário consegue formular consultas subsequentes sem necessidade de reformulação ou de suporte externo? |

<p align="center">Fonte: Do autor (2026).</p>

---

### Subcaracterística: Proteção contra Erros do Usuário

<p align="center">Tabela 3 – Questões relativas à subcaracterística Proteção contra Erros do Usuário.</p>

| ID | Questão |
| :---: | :--- |
| **Q1.6** | O módulo de importação de histórico impede eficazmente o envio de arquivos em formatos inválidos (diferentes do PDF padrão emitido pelo SIGAA) e comunica o erro de forma clara ao usuário? |
| **Q1.7** | Em que proporção os arquivos PDF corrompidos ou fora do padrão SIGAA são corretamente identificados e bloqueados pelo sistema antes do processamento? |
| **Q1.8** | As mensagens de erro e de validação exibidas pela interface são suficientemente descritivas para que o usuário compreenda o problema e saiba como corrigi-lo sem auxílio externo? |

<p align="center">Fonte: Do autor (2026).</p>

---

### Subcaracterística: Acessibilidade

<p align="center">Tabela 4 – Questões relativas à subcaracterística Acessibilidade.</p>

| ID | Questão |
| :---: | :--- |
| **Q1.9** | Os elementos interativos críticos da plataforma (botões de upload, nós do grafo de disciplinas, campos de busca) atendem aos critérios mínimos de contraste visual definidos pelas diretrizes WCAG 2.1? |
| **Q1.10** | A interface permite a operação completa das funcionalidades principais por meio de navegação exclusiva via teclado, sem dependência de interações por mouse ou toque? |
| **Q1.11** | Os componentes interativos da interface possuem atributos semânticos (como `aria-label` e `role`) que viabilizam a utilização por leitores de tela, garantindo acesso a estudantes com deficiência visual? |

<p align="center">Fonte: Do autor (2026).</p>

---

## Questões do Objetivo 2: Avaliação de Eficiência de Desempenho

As questões a seguir derivam do [Objetivo GQM 2 — Eficiência de Desempenho](./gqm_objetivo.md#objetivo2) e buscam operacionalizar a avaliação da subcaracterística de **Comportamento em Relação ao Tempo** e **Capacidade**, conforme definida em [Tabela 3 — Eficiência de Desempenho](../fase_1_v2/caracteristicas.md#eficiencia). A natureza das integrações do sistema — leitura de PDF do SIGAA, chamadas externas à API do **Darcy AI (Maritaca AI)** e renderização de grafos — torna o desempenho temporal um fator crítico para a experiência do usuário.

### Subcaracterística: Comportamento em Relação ao Tempo

<p align="center">Tabela 5 – Questões relativas à subcaracterística Comportamento em Relação ao Tempo.</p>

| ID | Questão |
| :---: | :--- |
| **Q2.1** | Qual é o tempo médio total decorrido entre o envio do arquivo PDF do histórico escolar pelo usuário e a renderização completa do grafo do fluxograma na tela, em condições normais de rede e infraestrutura? |
| **Q2.2** | Qual é o tempo médio de resposta do **Assistente Darcy AI** entre o envio de uma consulta pelo usuário e a exibição da resposta gerada, considerando a latência da API externa da Maritaca AI? |
| **Q2.3** | Em que medida a instabilidade ou oscilação no tempo de resposta da API da Maritaca AI impacta o tempo total de interação percebido pelo usuário no módulo do **Assistente Darcy AI**? |
| **Q2.4** | Como o tempo de processamento do módulo de importação de histórico (leitura e extração de dados do PDF) varia em cenários de uso simultâneo, simulando os períodos críticos de matrícula na UnB, em comparação com acessos isolados? |
| **Q2.5** | A interface fornece ao usuário sinalizações visuais de progresso (ex.: indicadores de carregamento) durante operações de processamento prolongado, de modo a reduzir a percepção de latência? |
| **Q2.6** | O sistema mantém estabilidade operacional ao processar históricos escolares com grande volume de disciplinas acumuladas ou extensões curriculares variadas, sem apresentar estouro de memória, travamentos ou falhas na comunicação com a API? |

<p align="center">Fonte: Do autor (2026).</p>

---

## Relacionamento Objetivo → Questões

A tabela abaixo consolida o mapeamento entre os objetivos de medição e suas respectivas questões, conforme o paradigma GQM de acordo com [Ramos (2025)](#ref01). O relacionamento foi estruturado de modo a garantir rastreabilidade entre as necessidades de qualidade identificadas na [Fase 1](../fase_1_v2/caracteristicas.md) e as questões que nortearão a definição das métricas na próxima etapa.

<p align="center">Tabela 6 – Relacionamento entre Objetivos GQM e Questões.</p>

| Objetivo | Subcaracterística | ID da Questão | Enunciado Resumido da Questão |
| :---: | :--- | :---: | :--- |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Reconhecimento da Adequação | [Q1.1](#q11-questão) | Comunicação imediata do propósito da tela inicial ao usuário. |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Reconhecimento da Adequação | [Q1.2](#q12-questão) | Clareza dos elementos visuais da interface inicial sobre as funcionalidades disponíveis. |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Capacidade de Aprendizado | [Q1.3](#q13-questão) | Tempo para completar o fluxo de importação e visualização no primeiro acesso. |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Capacidade de Aprendizado | [Q1.4](#q14-questão) | Suficiência das pistas visuais do Meu Fluxograma para compreensão autônoma do grafo. |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Capacidade de Aprendizado | [Q1.5](#q15-questão) | Autonomia do usuário em consultas subsequentes ao Assistente Darcy AI. |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Proteção contra Erros | [Q1.6](#q16-questão) | Eficácia do bloqueio de arquivos inválidos e clareza da mensagem de erro. |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Proteção contra Erros | [Q1.7](#q17-questão) | Proporção de PDFs corrompidos ou fora do padrão corretamente identificados. |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Proteção contra Erros | [Q1.8](#q18-questão) | Clareza e utilidade das mensagens de erro para a correção autônoma pelo usuário. |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Acessibilidade | [Q1.9](#q19-questão) | Conformidade dos elementos críticos com os critérios de contraste visual (WCAG 2.1). |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Acessibilidade | [Q1.10](#q110-questão) | Operabilidade completa via teclado, sem dependência de mouse ou toque. |
| [**Obj. 1**](./gqm_objetivo.md#objetivo-1-avaliacao-de-usabilidade) — Usabilidade | Acessibilidade | [Q1.11](#q111-questão) | Presença de atributos semânticos para compatibilidade com leitores de tela. |
| [**Obj. 2**](./gqm_objetivo.md#objetivo-2-avaliacao-de-eficiencia-de-desempenho) — Eficiência | Comportamento em Relação ao Tempo | [Q2.1](#q21-questão) | Tempo médio de ponta a ponta entre upload do PDF e renderização completa do grafo. |
| [**Obj. 2**](./gqm_objetivo.md#objetivo-2-avaliacao-de-eficiencia-de-desempenho) — Eficiência | Comportamento em Relação ao Tempo | [Q2.2](#q22-questão) | Tempo médio de resposta do Assistente Darcy AI por consulta. |
| [**Obj. 2**](./gqm_objetivo.md#objetivo-2-avaliacao-de-eficiencia-de-desempenho) — Eficiência | Comportamento em Relação ao Tempo | [Q2.3](#q23-questão) | Impacto da oscilação da API da Maritaca AI no tempo percebido pelo usuário. |
| [**Obj. 2**](./gqm_objetivo.md#objetivo-2-avaliacao-de-eficiencia-de-desempenho) — Eficiência | Comportamento em Relação ao Tempo | [Q2.4](#q24-questão) | Variação do tempo de processamento do upload em cenários de uso simultâneo. |
| [**Obj. 2**](./gqm_objetivo.md#objetivo-2-avaliacao-de-eficiencia-de-desempenho) — Eficiência | Comportamento em Relação ao Tempo | [Q2.5](#q25-questão) | Presença de sinalizações visuais de progresso para reduzir percepção de latência. |
 [**Obj. 2**](./objetivo.md#objetivo-2-avaliacao-de-eficiencia-de-desempenho) — Eficiência | Comportamento em Relação ao Tempo | [Q2.6](#q26-questão) | Estabilidade do sistema ao processar históricos com grande volume de disciplinas ou extensões curriculares variadas. |

<p align="center">Fonte: Do autor (2026).</p>

---

## Referências

<a id="ref01"></a>RAMOS, Cristiane Soares. **Medição baseada em objetivos — Goal-Question-Metric (GQM)**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025. Material de aula da disciplina FGA0278 — Qualidade de Software 1. Baseado no material da Profa. Dra. Káthia Marçal Oliveira. Disponível em: [slide_gqm.pdf](../assets/referencia/slide_gqm.pdf).

<a id="ref02"></a>BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, H. Dieter. **Goal Question Metric Paradigm**. In: MARCINIAK, John J. (Ed.). *Encyclopedia of Software Engineering*. 2. ed. New York: Wiley, 2002.

<a id="ref03"></a>NO FLUXO UNB. **Plataforma de acompanhamento e planejamento de fluxo acadêmico**. Versão 1.0. Brasília: Crianex, 2026. Disponível em: [https://no-fluxo.crianex.com/](https://no-fluxo.crianex.com/). Acesso em: 5 jun. 2026.

---

## Declaração do uso de IA

Eu, [Ana Luiza](https://github.com/Ana-Luiza-SC), declaro que utilizei a ferramenta Claude (Anthropic) para apoio na estruturação e redação das questões GQM, tendo o conteúdo sido revisado e validado pela equipe.

---

## Histórico de Versão

| Versão | Data | Descrição | Autor |
|---|---|---|---|
| 1.0 | 07/06/26 | Escrita das questões GQM e tabela de relacionamento | Ana Luiza |