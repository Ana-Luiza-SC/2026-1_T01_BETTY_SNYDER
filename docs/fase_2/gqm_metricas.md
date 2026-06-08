# Métricas, Níveis de Pontuação e Critérios de Julgamento GQM

Esta seção apresenta a estruturação das métricas, escalas de pontuação e critérios de julgamento derivados do desdobramento do paradigma *Goal-Question-Metric* (GQM) para o [No Fluxo UnB](#ref03). As métricas operacionalizam as questões formuladas, estabelecendo limiares objetivos alinhados com as hipóteses de linha de base e justificativas técnicas da plataforma.

---

## 1. Mapeamento de Métricas por Objetivo

As métricas foram selecionadas considerando a abordagem caixa-preta da avaliação, com foco em medições de percepção de tempo de execução, conformidade técnica externa e observação direta do comportamento do usuário.

### Mapeamento do Objetivo 1: Usabilidade

<p align="center">Tabela 1 – Métricas para a avaliação de Usabilidade.</p>

| ID Questão | ID Métrica | Nome da Métrica | Tipo de Dado | Descrição Operacional |
| :---: | :---: | :--- | :---: | :--- |
| **Q1.1** | **M1.1** | Taxa de Acerto no Teste de Adequação de 5 Segundos | Percentual | Proporção de usuários em teste que identificam o propósito central da plataforma após visualizarem a tela inicial por 5 segundos. |
| **Q1.2** | **M1.2** | Índice de Clareza Autoavaliada da Interface | Escala (1 a 5) | Nota atribuída pelo usuário em relação à clareza visual dos botões e ícones da página inicial. |
| **Q1.3** | **M1.3** | Tempo de Execução do Primeiro Fluxo Crítico | Segundos | Tempo cronometrado entre o primeiro acesso do estudante e a conclusão visual da renderização do grafo. |
| **Q1.4** | **M1.4** | Taxa de Compreensão Autônoma de Legendas | Percentual | Percentual de nós e cores do grafo interpretados corretamente pelo usuário sem auxílio externo. |
| **Q1.5** | **M1.5** | Taxa de Iterações Diretas com Darcy AI | Percentual | Proporção de interações com o assistente de IA que não exigiram reformulação de pergunta pelo usuário. |
| **Q1.6** | **M1.6** | Eficácia do Bloqueio de Extensões Inválidas | Percentual | Percentual de arquivos com extensões incorretas barrados imediatamente pela interface. |
| **Q1.7** | **M1.7** | Taxa de Interceptação de PDFs Corrompidos | Percentual | Proporção de PDFs corrompidos ou fora do padrão do SIGAA que foram rejeitados no front-end. |
| **Q1.8** | **M1.8** | Índice de Correção Autônoma Baseada em Mensagem | Percentual | Percentual de usuários que conseguem corrigir o arquivo enviado após lerem a mensagem de erro da tela. |
| **Q1.9** | **M1.9** | Taxa de Conformidade de Contraste (WCAG 2.1) | Percentual | Proporção de botões, textos e nós do grafo que atendem à taxa de contraste mínima exigida por ferramentas de auditoria. |
| **Q1.10** | **M1.10** | Cobertura de Operabilidade via Teclado | Percentual | Percentual de funcionalidades críticas da interface que podem ser executadas exclusivamente via teclado. |
| **Q1.11** | **M1.11** | Densidade de Atributos Semânticos Acessíveis | Percentual | Proporção de componentes de interação mapeados com tags `aria-label` ou `role` adequadas. |

<p align="center">Fonte: Do autor (2026).</p>

---

### Mapeamento do Objetivo 2: Eficiência de Desempenho

<p align="center">Tabela 2 – Métricas para a avaliação de Eficiência de Desempenho.</p>

| ID Questão | ID Métrica | Nome da Métrica | Tipo de Dado | Descrição Operacional |
| :---: | :---: | :--- | :---: | :--- |
| **Q2.1** | **M2.1** | Tempo de Resposta de Ponta a Ponta do Fluxograma | Segundos | Tempo decorrido do clique de upload do PDF até a renderização visual e completa do grafo na tela. |
| **Q2.2** | **M2.2** | Tempo Médio de Resposta do Assistente Darcy AI | Segundos | Intervalo temporal medido entre o envio de um comando no chat e o retorno em texto da resposta da IA. |
| **Q2.3** | **M2.3** | Desvio Padrão por Instabilidade da Maritaca API | Segundos | Variabilidade encontrada nas medições de tempo da IA quando o serviço externo apresenta oscilação de latência. |
| **Q2.4** | **M2.4** | Fator de Degradação sob Concorrência Simulada | Percentual | Aumento percentual no tempo de processamento de arquivos ao executar requisições síncronas simultâneas. |
| **Q2.5** | **M2.5** | Cobertura de Sinalizações Visuais de Progresso | Percentual | Proporção de processos com tempo de execução superior a 2 segundos que possuem spinners ou barras de carregamento. |
| **Q2.6** | **M2.6** | Taxa de Sucesso no Processamento de Altas Cargas | Percentual | Percentual de históricos com grande volume de semestres ou extensões curriculares processados sem erros de estouro de memória. |

<p align="center">Fonte: Do autor (2026).</p>

---

## 2. Níveis de Pontuação e Escalas de Avaliação

Cada métrica possui limiares específicos categorizados em três níveis de desempenho: **Inadequado**, **Regular** e **Adequado**. Os valores de corte foram calibrados com base nas hipóteses de linha de base (H1 a H7) estabelecidas para o projeto.

<p align="center">Tabela 3 – Níveis de pontuação estabelecidos para as métricas GQM.</p>

| ID Métrica | Unidade | Inadequado (Crítico) | Regular (Alerta) | Adequado (Meta) | Referência de Alinhamento |
| :---: | :---: | :--- | :--- | :--- | :--- |
| **M1.1** | % | Abaixo de 60% | De 60% a 79% | 80% ou mais | Hipótese H4 (> 80% reconhecimento imediato) |
| **M1.2** | Nota | Abaixo de 3.0 | De 3.0 a 3.9 | 4.0 ou mais | Mapeamento de usabilidade percebida |
| **M1.3** | Minutos | Mais de 3 min | De 2 a 3 min | Menos de 2 min | Hipótese H1 (< 2 minutos no primeiro acesso) |
| **M1.4** | % | Abaixo de 70% | De 70% a 89% | 90% ou mais | Compreensão visual autônoma do Meu Fluxograma |
| **M1.5** | % | Abaixo de 50% | De 50% a 74% | 75% ou mais | Autonomia em consultas ao Assistente Darcy AI |
| **M1.6** | % | Abaixo de 90% | De 90% a 99% | 100% | Proteção rigorosa de entrada de arquivos inválidos |
| **M1.7** | % | Abaixo de 80% | De 80% a 94% | 95% ou mais | Hipótese H2 (Barramento de 95% de arquivos corrompidos) |
| **M1.8** | % | Abaixo de 60% | De 60% a 79% | 80% ou mais | Correção de erros orientada por mensagens descritivas |
| **M1.9** | % | Abaixo de 70% | De 70% a 84% | 85% ou mais | Critérios mínimos de contraste WCAG 2.1 |
| **M1.10** | % | Abaixo de 80% | De 80% a 99% | 100% | Operabilidade completa por teclado para acessibilidade |
| **M1.11** | % | Abaixo de 50% | De 50% a 79% | 80% ou mais | Hipótese H3 (Acessibilidade para leitores de tela) |
| **M2.1** | Segundos | Mais de 6 seg | De 4 a 6 seg | Menos de 4 seg | Hipótese H5 (< 4 segundos para processar e renderizar) |
| **M2.2** | Segundos | Mais de 8 seg | De 5 a 8 seg | Menos de 5 seg | Latência aceitável esperada em interfaces conversacionais |
| **M2.3** | Segundos | Mais de 4 seg | De 2.1 a 4 seg | 2 seg ou menos | Hipótese H6 (Impacto de oscilação da API Maritaca AI) |
| **M2.4** | % | Mais de 50% | De 41% a 50% | 40% ou menos | Hipótese H7 (Aumento de até 40% sob concorrência) |
| **M2.5** | % | Abaixo de 80% | De 80% a 99% | 100% | Mitigação de percepção de latência via sinalização visual |
| **M2.6** | % | Abaixo de 90% | De 90% a 99% | 100% | Estabilidade operacional em fluxos de alta carga |

<p align="center">Fonte: Do autor (2026).</p>

---

## 3. Critérios de Julgamento Global

Para interpretar os resultados coletados nas fases de medição e emitir um parecer sobre a qualidade do software, foram definidos critérios de agregação baseados na criticidade e representatividade das subcaracterísticas estudadas.

### Regra de Consolidação por Subcaracterística

* **Adequada:** A subcaracterística será considerada adequada se todas as suas métricas obrigatórias atingirem o nível Adequado e nenhuma métrica acessória estiver no nível Inadequado.
* **Em Alerta:** A subcaracterística entrará em nível de alerta se qualquer uma de suas métricas estiver na faixa Regular ou se apresentar métricas acessórias em nível Inadequado.
* **Inadequada:** A subcaracterística será classificada como inadequada caso qualquer métrica obrigatória seja pontuada na faixa Inadequada.

### Julgamento dos Objetivos de Medição

> **Parecer do Objetivo 1 (Usabilidade):**
> A interface será declarada intuitiva e acessível se as subcaracterísticas de *Proteção contra Erros* e *Capacidade de Aprendizado* forem consolidadas como Adequadas. Caso fiquem em nível de Alerta, serão recomendadas correções prioritárias de layout e refatoração de feedbacks visuais.

> **Parecer do Objetivo 2 (Eficiência de Desempenho):**
> O ecossistema de software será classificado como eficiente se o *Comportamento em Relação ao Tempo* for consolidado como Adequado sob uso isolado. Pontuações regulares nas métricas de concorrência dispararão a necessidade de implementação de filas assíncronas no tratamento de dados e técnicas de cache no front-end para otimizar a renderização de grafos.

---

## Referências

<a id="ref01"></a>RAMOS, Cristiane Soares. **Medição baseada em objetivos — Goal-Question-Metric (GQM)**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025. Material de aula da disciplina FGA0278 — Qualidade de Software 1. Baseado no material da Profa. Dra. Káthia Marçal Oliveira. Disponível em: [slide_gqm.pdf](../assets/referencia/slide_gqm.pdf).

<a id="ref02"></a>BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, H. Dieter. **Goal Question Metric Paradigm**. In: MARCINIAK, John J. (Ed.). *Encyclopedia of Software Engineering*. 2. ed. New York: Wiley, 2002.

<a id="ref03"></a>NO FLUXO UNB. **Plataforma de acompanhamento e planejamento de fluxo acadêmico**. Versão 1.0. Brasília: Crianex, 2026. Disponível em: [https://no-fluxo.crianex.com/](https://no-fluxo.crianex.com/). Acesso em: 5 jun. 2026.

---

## Declaração do uso de IA

Eu, Daniel Rodrigues Nascimento, declaro que utilizei a inteligência artificial Gemini para o mapeamento lógico e operacional das métricas a partir das questões pré-definidas no GQM, estruturando as tabelas de limiares de pontuação e os critérios de agregação de pareceres conforme os padrões formais de Engenharia de Software e Qualidade de Produto.

---

## Histórico de Versão

| Versão | Data | Descrição | Autor |
| :---: | :---: | :--- | :--- |
| 1.0 | 08/06/26 | Criação do documento contendo mapeamento de métricas, níveis de pontuação e critérios de julgamento global GQM. | Daniel Rodrigues Nascimento |