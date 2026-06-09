#  Método de Avaliação

Esta seção documenta o método de avaliação que será utilizado na avaliação do **No Fluxo UnB**, o ambiente de execução e os recursos necessários. O método de avaliação foi escolhido e adequado com base nos requisitos de qualidade definidos na [Fase 1](../fase_1_v2/caracteristicas.md) e nas especificações de métricas e critérios estabelecidos na [Fase 2](../fase_2/gqm_metricas.md), seguindo o processo de avaliação de produto de software conforme as diretrizes da série ISO/IEC 25000 (SQuaRE).

---

## 1. Método de Avaliação

A avaliação adota uma abordagem de **caixa-preta** sobre o sistema disponível em ambiente de produção (https://no-fluxo.crianex.com/), sem acesso ao código-fonte ou à infraestrutura interna. Os métodos foram selecionados em função das características de qualidade priorizadas (Usabilidade e Eficiência de Desempenho) e das restrições operacionais do projeto.

### 1.1 Métodos por Objetivo de Medição

#### Objetivo 1 — Avaliação de Usabilidade

| Subcaracterística | Método Aplicado | Instrumento |
| :--- | :--- | :--- |
| **Reconhecimento da Adequação** | Teste dos 5 Segundos (*Five-Second Test*) com usuários reais | Formulário de coleta pós-exposição |
| **Capacidade de Aprendizado** | Teste de usabilidade com observação direta (*Think Aloud*) | Roteiro de tarefas + cronômetro |
| **Proteção contra Erros do Usuário** | Teste exploratório com injeção de entradas inválidas | Checklist de cobertura de erros |
| **Acessibilidade** | Inspeção automatizada com ferramentas de auditoria (Lighthouse / axe DevTools) + verificação manual de navegação via teclado | Relatório de auditoria + checklist WCAG 2.1 |

#### Objetivo 2 — Avaliação de Eficiência de Desempenho

| Subcaracterística | Método Aplicado | Instrumento |
| :--- | :--- | :--- |
| **Comportamento em Relação ao Tempo** | Medição cronometrada de tempo de ponta a ponta nas operações críticas | Cronômetro manual + ferramentas de rede do navegador (DevTools > Network) |
| **Capacidade** | Execução de cenários de carga moderada com múltiplos arquivos e simulação de uso simultâneo | Históricos escolares fictícios de diferentes complexidades |

---

## Referências

<a id="ref01"></a>INTERNATIONAL ORGANIZATION FOR STANDARDIZATION (ISO). **ISO/IEC 25000:2014 — Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — Guide to SQuaRE**. Geneva: ISO, 2014. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards>.

<a id="ref02"></a>RAMOS, Cristiane Soares. **Processo de Avaliação de Produto de Software**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025. Material de aula da disciplina FGA0278 — Qualidade de Software 1.

<a id="ref03"></a>RAMOS, Cristiane Soares. **Medição baseada em objetivos — Goal-Question-Metric (GQM)**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025. Material de aula da disciplina FGA0278 — Qualidade de Software 1.

<a id="ref04"></a>BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, H. Dieter. **Goal Question Metric Paradigm**. In: MARCINIAK, John J. (Ed.). *Encyclopedia of Software Engineering*. 2. ed. New York: Wiley, 2002.

<a id="ref05"></a>NO FLUXO UNB. **Plataforma de acompanhamento e planejamento de fluxo acadêmico**. Versão 1.0. Brasília: Crianex, 2026. Disponível em: <https://no-fluxo.crianex.com/>. Acesso em: 9 jun. 2026.

<a id="ref06"></a>WORLD WIDE WEB CONSORTIUM (W3C). **Web Content Accessibility Guidelines (WCAG) 2.1**. W3C Recommendation, 2018. Disponível em: <https://www.w3.org/TR/WCAG21/>.

---

## Declaração do uso de IA

Eu, [nome do autor], declaro que utilizei a ferramenta Claude (Anthropic) para apoio na estruturação e redação deste plano de avaliação, tendo o conteúdo sido revisado e validado pela equipe.

---

## Histórico de Versão

| Versão | Data | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| 1.0 | 09/06/26 | Criação do documento de Plano de Avaliação (Fase 3) | — |