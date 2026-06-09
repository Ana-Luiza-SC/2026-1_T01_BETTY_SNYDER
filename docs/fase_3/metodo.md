# Método de Avaliação

Esta seção documenta o método de avaliação que será utilizado na avaliação do **No Fluxo UnB** (NO FLUXO UNB, 2026), o ambiente de execução e os recursos necessários. O método de avaliação foi escolhido e adequado com base nos requisitos de qualidade definidos na [Fase 1](../fase_1_v2/caracteristicas.md) e nas especificações de métricas e critérios estabelecidos na [Fase 2](../fase_2/gqm_metricas.md), seguindo o processo de avaliação de produto de software conforme as diretrizes da série ISO/IEC 25000 (SQuaRE) (ISO, 2014).

---

## 1. Método de Avaliação

A avaliação adota uma abordagem de **caixa-preta** sobre o sistema disponível em ambiente de produção (https://no-fluxo.crianex.com/) (NO FLUXO UNB, 2026), sem acesso ao código-fonte ou à infraestrutura interna. Os métodos foram selecionados em função das características de qualidade priorizadas (Usabilidade e Eficiência de Desempenho) e das restrições operacionais do projeto, alinhando-se aos conceitos fundamentais do paradigma de medição orientada a objetivos (BASILI; CALDIERA; ROMBACH, 2002). A tabela contendo o tipo de dado e a descrição operacional de cada métrica pode ser encontrada na subseção [GQM - Metrics](../fase_2/gqm_metricas.md/#1-mapeamento-de-métricas-por-objetivo), a qual foi estruturada seguindo as diretrizes metodológicas para a especificação de métricas de software (RAMOS, 2025b).

### 1.1 Métodos de Avaliação para cada Métrica

#### Objetivo 1 — Usabilidade

| ID | Métrica | Subcaracterística | Método de Avaliação | Instrumento |
| :---: | :--- | :--- | :--- | :--- |
| **M1.1** | Taxa de Acerto no Teste de Adequação de 5 Segundos | Reconhecimento da Adequação | Teste dos 5 Segundos com usuários reais | Formulário de coleta pós-exposição |
| **M1.2** | Índice de Clareza Autoavaliada da Interface | Reconhecimento da Adequação | Questionário pós-teste com escala Likert | Formulário de coleta pós-exposição |
| **M1.3** | Tempo de Execução do Primeiro Fluxo Crítico | Capacidade de Aprendizado | Teste de usabilidade com observação direta (Think Aloud) | Roteiro de tarefas + cronômetro |
| **M1.4** | Taxa de Compreensão Autônoma de Legendas | Capacidade de Aprendizado | Teste de usabilidade com observação direta (Think Aloud) | Roteiro de tarefas + cronômetro |
| **M1.5** | Taxa de Iterações Diretas com Darcy AI | Capacidade de Aprendizado | Teste de usabilidade com observação direta (Think Aloud) | Roteiro de tarefas + registro de interações |
| **M1.6** | Eficácia do Bloqueio de Extensões Inválidas | Proteção contra Erros do Usuário | Teste exploratório com injeção de entradas inválidas | Checklist de cobertura de erros |
| **M1.7** | Taxa de Interceptação de PDFs Corrompidos | Proteção contra Erros do Usuário | Teste exploratório com injeção de entradas inválidas | Checklist de cobertura de erros |
| **M1.8** | Índice de Correção Autônoma Baseada em Mensagem | Proteção contra Erros do Usuário | Teste de usabilidade com observação direta (Think Aloud) | Roteiro de tarefas + registro de comportamento |
| **M1.9** | Taxa de Conformidade de Contraste (WCAG 2.1) (W3C, 2018) | Acessibilidade | Auditoria automatizada | Relatório de auditoria |
| **M1.10** | Cobertura de Operabilidade via Teclado (W3C, 2018) | Acessibilidade | Teste manual de navegação | Checklist WCAG 2.1 |
| **M1.11** | Densidade de Atributos Semânticos Acessíveis (W3C, 2018) | Acessibilidade | Inspeção estática do código HTML da página | Relatório de auditoria |

---

#### Objetivo 2 — Eficiência de Desempenho

| ID | Métrica | Subcaracterística | Método de Avaliação | Instrumento |
| :---: | :--- | :--- | :--- | :--- |
| **M2.1** | Tempo de Resposta de Ponta a Ponta do Fluxograma | Comportamento em Relação ao Tempo | Medição cronometrada de operações críticas (ponta a ponta) | Cronômetro manual + Inspeção manual |
| **M2.2** | Tempo Médio de Resposta do Assistente Darcy AI | Comportamento em Relação ao Tempo | Medição cronometrada de operações críticas (ponta a ponta) | Cronômetro manual + Inspeção manual |
| **M2.3** | Desvio Padrão por Instabilidade da Maritaca API | Comportamento em Relação ao Tempo | Medição cronometrada com múltiplas repetições | DevTools > Network + análise estatística |
| **M2.4** | Fator de Degradação sob Concorrência Simulada | Capacidade | Execução de cenários de carga com requisições síncronas simultâneas | Históricos fictícios de diferentes complexidades |
| **M2.5** | Cobertura de Sinalizações Visuais de Progresso | Capacidade | Inspeção de interface durante operações longas (> 2s) | Checklist de cobertura + cronômetro |
| **M2.6** | Taxa de Sucesso no Processamento de Altas Cargas | Capacidade | Execução de cenários de carga com múltiplos arquivos | Históricos fictícios de diferentes complexidades |

---

## 2. Ambiente e Recursos Necessários para a Avaliação

Para garantir a execução e qualidade da avaliação do software, a seguir encontram-se as condições de infraestrutura, os recursos humanos e o ferramental tecnológico necessários para sua realização.

### 2.1 Ambiente de Execução e Conectividade
* **Instância Alvo:** Toda a atividade avaliativa ocorrerá por meio de testes baseados no comportamento de caixa-preta da aplicação web ativa e pública na URL oficial da plataforma No Fluxo UnB (NO FLUXO UNB, 2026).
* **Condições de Rede:** Os computadores utilizados pelos avaliadores e participantes deverão dispor de acesso estável à internet banda larga. Isso é indispensável para evitar ruídos e discrepâncias externas nas medições de comportamento em relação ao tempo e latência de rede.

### 2.2 Recursos Humanos
* **Avaliadores:** Integrantes da equipe técnica responsáveis por estruturar os roteiros de teste, guiar os usuários na técnica *Think Aloud*, cronometrar tarefas, disparar injeções de erro em testes exploratórios e conduzir auditorias de acessibilidade.
* **Usuários Participantes:** Grupo de amostragem composto por estudantes universitários para simular interações reais com a interface e responder aos instrumentos de percepção subjetiva, como o teste de cinco segundos e questionários Likert.

### 2.3 Ferramentas e Instrumentos Tecnológicos
A consolidação das coletas práticas requer o emprego dos seguintes recursos tecnológicos:

#### 2.3.1 Ambiente de Hardware
* **Desktop / Notebook:** Notebooks com os sistemas operacionais Windows 11, Ubuntu 22.04 LTS (ou versão equivalente) e macOS Sonoma, utilizados como ambiente primário para a execução dos testes funcionais e de portabilidade.

#### 2.3.2 Ambiente de Software
* **Navegadores Web com Console de Desenvolvedor (DevTools):** Ferramentas nativas de inspeção (como *Chrome DevTools* ou *Firefox Developer Tools*) com foco nas abas *Network* (Rede) para capturar o tempo exato das requisições e processamento da Maritaca API (M2.3), e *Elements* para inspeção estática da estrutura semântica da árvore DOM (M1.11).
* **Validadores Automatizados de Acessibilidade:** Uso de extensões especializadas para auditoria de conformidade com as diretrizes WCAG 2.1 (W3C, 2018), tais como *Lighthouse*, *Axe DevTools* ou *WAVE Mobile and Web Accessibility Evaluation Tool*, para medir com exatidão a conformidade de contraste (M1.9).
* **Massa de Dados e Carga de Arquivos:** Conjunto controlado de dados simulados contendo:
  * Históricos escolares fictícios em formato PDF estruturados em diferentes níveis de complexidade (M2.4 e M2.6);
  * Arquivos intencionalmente corrompidos ou em extensões inválidas (como `.docx`, `.png`, `.txt`) para avaliar a capacidade de tratamento de erros da aplicação (M1.6 e M1.7).

#### 2.3.3 Ferramentas de Coleta
* **Roteiros de tarefas:** Roteiros com as tarefas para direcionar os participantes.
* **Cronômetros:** Cronômetros para realizar os testes que necessitam de medição de tempo.
* **Teams:** Será utilizado para a gravação da tela dos testes de usabilidade com os usuários.
* **Documento de Registro:** Artefato destinado a anotar os dados qualitativos e/ou quantitativos coletados durante os testes.

---

## Referências

<a id="ref01"></a>[1] INTERNATIONAL ORGANIZATION FOR STANDARDIZATION (ISO). **ISO/IEC 25000:2014 — Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — Guide to SQuaRE**. Geneva: ISO, 2014. Disponível em: [https://iso25000.com/index.php/en/iso-25000-standards](https://iso25000.com/index.php/en/iso-25000-standards).

<a id="ref02"></a>[2] RAMOS, Cristiane Soares. **Processo de Avaliação de Produto de Software**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025a. Material de aula da disciplina FGA0278 — Qualidade de Software 1.

<a id="ref03"></a>[3] RAMOS, Cristiane Soares. **Medição baseada em objetivos — Goal-Question-Metric (GQM)**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025b. Material de aula da disciplina FGA0278 — Qualidade de Software 1. Baseado no material da Profa. Dra. Káthia Marçal Oliveira. Disponível em: [slide_gqm.pdf](../assets/referencia/slide_gqm.pdf).

<a id="ref05"></a>[5] NO FLUXO UNB. **Plataforma de acompanhamento e planejamento de fluxo acadêmico**. Versão 1.0. Brasília: Crianex, 2026. Disponível em: [https://no-fluxo.crianex.com/](https://no-fluxo.crianex.com/). Acesso em: 9 jun. 2026.

<a id="ref06"></a>[6] WORLD WIDE WEB CONSORTIUM (W3C). **Web Content Accessibility Guidelines (WCAG) 2.1**. W3C Recommendation, 2018. Disponível em: [https://www.w3.org/TR/WCAG21/](https://www.w3.org/TR/WCAG21/).

---

## Declaração do uso de IA

Eu, Ígor Veras Daniel, declaro que utilizei a ferramenta Gemini (Google) para apoio na estruturação e redação deste plano de avaliação, tendo o conteúdo sido revisado e validado pela equipe.

---

## Histórico de Versão

| Versão | Data | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| 1.0 | 09/06/26 | Criação do documento de Plano de Avaliação (Fase 3) | Ígor Veras |