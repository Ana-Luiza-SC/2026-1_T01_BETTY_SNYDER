## 1. Massa de Dados

A massa de dados definida para a avaliação do **No Fluxo UnB** foi estruturada de acordo com os objetivos GQM, questões de avaliação e métricas especificadas na Fase 2. Como a avaliação será conduzida em abordagem de caixa-preta, os dados utilizados têm como finalidade simular interações reais de estudantes com a plataforma, além de permitir a verificação de cenários de erro, acessibilidade e desempenho.

### 1.1 Conjuntos de Dados Utilizados

| Conjunto                                           | Descrição                                                                                                                                                                                 | Métricas Relacionadas                      |
| :------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------- |
| **MD1 — Participantes da Avaliação**               | Grupo de estudantes universitários que executarão tarefas de uso real da plataforma, responderão questionários e participarão dos testes de usabilidade.                                  | M1.1, M1.2, M1.3, M1.4, M1.5, M1.8         |
| **MD2 — Históricos Escolares Válidos**             | Arquivos PDF fictícios ou anonimizados, em formato compatível com o padrão de histórico escolar do SIGAA, utilizados para testar o fluxo principal de importação e geração do fluxograma. | M1.3, M2.1, M2.4, M2.6                     |
| **MD3 — Arquivos Inválidos**                       | Arquivos com extensões não aceitas pela aplicação, como `.docx`, `.png`, `.jpg` e `.txt`, utilizados para verificar o bloqueio de entradas inválidas.                                     | M1.6                                       |
| **MD4 — PDFs Corrompidos ou Fora do Padrão SIGAA** | Arquivos PDF danificados, incompletos ou sem a estrutura esperada de um histórico escolar, usados para avaliar a proteção contra erros no processamento.                                  | M1.7, M1.8                                 |
| **MD5 — Consultas Padronizadas ao Darcy AI**       | Conjunto de perguntas previamente definidas sobre fluxo acadêmico, pré-requisitos, disciplinas disponíveis, integralização curricular e planejamento de matrícula.                        | M1.5, M2.2, M2.3                           |
| **MD6 — Elementos de Interface Avaliados**         | Telas e componentes críticos da interface, como tela inicial, botão de upload, grafo de disciplinas, campos de busca, mensagens de erro e área do Assistente Darcy AI.                    | M1.1, M1.2, M1.4, M1.9, M1.10, M1.11, M2.5 |

### 1.2 Massa de Dados para Históricos Escolares

Os históricos escolares utilizados na avaliação serão classificados por complexidade, de modo a permitir a análise do comportamento da aplicação em diferentes volumes de dados.

| Tipo de Histórico             | Quantidade Recomendada | Finalidade                                                                                                          |
| :---------------------------- | :--------------------: | :------------------------------------------------------------------------------------------------------------------ |
| Histórico pequeno             |            3           | Simular estudantes em início de curso, com poucas disciplinas cursadas.                                             |
| Histórico médio               |            3           | Simular estudantes em andamento regular no curso.                                                                   |
| Histórico grande              |            3           | Simular estudantes próximos da conclusão, com maior volume de disciplinas, reprovações, optativas ou equivalências. |
| Histórico fora do padrão      |            3           | Verificar se o sistema identifica arquivos que não seguem o modelo esperado do SIGAA.                               |
| PDF corrompido                |            3           | Avaliar a interceptação de arquivos danificados antes do processamento.                                             |
| Arquivo com extensão inválida |            4           | Avaliar o bloqueio de formatos não permitidos pela interface.                                                       |

Quando forem utilizados históricos reais, os dados deverão ser anonimizados antes da execução dos testes, removendo nome, matrícula, CPF, e-mail ou qualquer outro dado pessoal do estudante.

### 1.3 Massa de Dados para Consultas ao Darcy AI

As consultas ao Assistente Darcy AI serão padronizadas para reduzir variações entre execuções e permitir comparação dos tempos de resposta.

| Categoria                | Exemplo de Consulta                                                       |
| :----------------------- | :------------------------------------------------------------------------ |
| Planejamento acadêmico   | “Quais disciplinas posso cursar no próximo semestre?”                     |
| Pré-requisitos           | “Quais disciplinas preciso concluir antes de cursar Estruturas de Dados?” |
| Fluxo curricular         | “Quais disciplinas estão bloqueadas no meu fluxo?”                        |
| Integralização           | “Quantos créditos faltam para eu me formar?”                              |
| Organização de matrícula | “Como posso organizar minha grade para evitar conflitos?”                 |

Cada consulta deverá ser executada mais de uma vez, registrando-se o tempo de resposta, eventuais falhas, mensagens de erro e variações perceptíveis no comportamento do assistente.

### 1.4 Critérios de Validação da Massa de Dados

Antes da execução da avaliação, a massa de dados deverá ser verificada segundo os seguintes critérios:

| Critério           | Descrição                                                                                                                                |
| :----------------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| Representatividade | Os dados devem representar cenários reais de uso do No Fluxo UnB por estudantes.                                                         |
| Cobertura          | A massa de dados deve contemplar fluxo normal, erro de entrada, arquivos corrompidos, consultas ao assistente e cenários de maior carga. |
| Anonimização       | Dados reais de estudantes não devem conter informações pessoais identificáveis.                                                          |
| Reprodutibilidade  | Os mesmos arquivos e consultas devem poder ser reutilizados em repetições futuras da avaliação.                                          |
| Rastreabilidade    | Cada conjunto de dados deve estar associado às métricas e questões GQM correspondentes.                                                  |

## Uso de IA

Declaro que nesse documento não fiz uso de IA para o seu desenvolvimento.

## Referências

<a id="ref02"></a> RAMOS, Cristiane Soares. **Processo de Avaliação de Produto de Software**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025a. Material de aula da disciplina FGA0278 — Qualidade de Software 1.

<a id="ref03"></a> RAMOS, Cristiane Soares. **Medição baseada em objetivos — Goal-Question-Metric (GQM)**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025b. Material de aula da disciplina FGA0278 — Qualidade de Software 1. Baseado no material da Profa. Dra. Káthia Marçal Oliveira. Disponível em: [slide_gqm.pdf](../assets/referencia/slide_gqm.pdf).

<a id="ref05"></a> NO FLUXO UNB. **Plataforma de acompanhamento e planejamento de fluxo acadêmico**. Versão 1.0. Brasília: Crianex, 2026. Disponível em: [https://no-fluxo.crianex.com/](https://no-fluxo.crianex.com/). Acesso em: 9 jun. 2026.


## Histórico de Versão

| Versão | Data | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| 1.0 | 09/06/26 | Criação do documento de Massa de Dados (Fase 3) | Julia Gabriela |
