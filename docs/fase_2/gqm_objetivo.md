Esta seção apresenta a definição formal dos objetivos de medição, hipóteses de linha de base e justificativas para o ecossistema **No Fluxo UnB**, seguindo a metodologia *Goal-Question-Metric* (GQM) [[1]](#ref01).

## Objetivos GQM

Foram mapeados dois focos principais de análise, alinhados às [características de qualidade selecionadas na Fase 1](../fase_1_v2/caracteristicas.md):

<a id="objetivo1"></a>

### Objetivo 1: Avaliação de Usabilidade

| Dimensão GQM | Definição do Objetivo |
| :--- | :--- |
| **Analisar** | A interface web do sistema *No Fluxo UnB* e seus fluxos de interação. |
| **Para o propósito de** | Avaliar e caracterizar. |
| **Com respeito ao foco de qualidade** | Usabilidade (focando especificamente nas subcaracterísticas de Reconhecimento da Adequação, Capacidade de Aprendizado, Proteção contra Erros do Usuário e Acessibilidade) — ver [Tabela 2 — Usabilidade](../fase_1_v2/caracteristicas.md#1-usabilidade). |
| **Do ponto de vista do/a** | Desenvolvedores (para identificar falhas de interface e fluxo), equipe de qualidade (para validar os requisitos de usabilidade) e usuários finais (como os estudantes da UnB, que necessitam de uma interface intuitiva) — ver [Stakeholders](../fase_1_v2/objetivo_avaliacao.md#stakeholder). |
| **No contexto de** | Utilização da plataforma web em dispositivos variados (computadores e celulares) e realização de tarefas cotidianas e críticas de planejamento acadêmico, tais como o upload do histórico escolar em PDF emitido pelo SIGAA e a interpretação/navegação visual pelo grafo do fluxograma de disciplinas — ver [Dentro do Escopo](../fase_1_v2/escopo.md#dentro-do-escopo) e [Funções Alvo da Avaliação](../fase_1_v2/descricao.md#funcoes-alvo-da-avaliacao). |

<center><sub>Tabela 1 — Objetivo GQM de Usabilidade.</sub></center>

<a id="objetivo2"></a>

### Objetivo 2: Avaliação de Eficiência de Desempenho

| Dimensão GQM | Definição do Objetivo |
| :--- | :--- |
| **Analisar** | O tempo de processamento e a comunicação de dados do ecossistema de software. |
| **Para o propósito de** | Compreender e avaliar. |
| **Com respeito ao foco de qualidade** | Eficiência de Desempenho (focando especificamente na subcaracterística de Comportamento em Relação ao Tempo) — ver [Tabela 3 — Eficiência de Desempenho](../fase_1_v2/caracteristicas.md#2-eficiencia-de-desempenho). |
| **Do ponto de vista do/a** | Equipe de desenvolvimento e infraestrutura (para identificar gargalos de processamento, falhas de integração e consumo de recursos) e administradores/operadores do sistema (para monitorar a estabilidade operacional e a latência da plataforma) — ver [Stakeholders](../fase_1_v2/objetivo_avaliacao.md#stakeholder). |
| **No contexto de** | Cenários de uso real da aplicação, envolvendo situações de alta demanda (como períodos de matrícula), o processamento sequencial de arquivos (leitura e extração de dados do PDF do histórico do SIGAA), a comunicação externa via API com o assistente Darcy AI (Maritaca AI) e a renderização síncrona dos grafos de disciplinas — ver [Cenário e Dados de Teste](../fase_1_v2/escopo.md#cenario-e-dados-de-teste) e [Cenário de Aplicação](../fase_1_v2/objetivo_avaliacao.md#cenario-de-aplicacao). |

<center><sub>Tabela 2 — Objetivo GQM de Eficiência de Desempenho.</sub></center>

## Hipóteses de Linha de Base

As hipóteses abaixo representam as expectativas iniciais e o conhecimento implícito da equipe de desenvolvimento (alinhados ao conceito de *Abstraction Sheet* [[1]](#ref01)), servindo como referencial comparativo para a futura fase de interpretação dos dados:

| ID | Característica | Subcaracterística | Descrição da Hipótese |
| :---: | :--- | :--- | :--- |
| **H1** | Usabilidade | Capacidade de Aprendizado | Espera-se que um estudante da UnB consiga carregar seu histórico escolar em formato PDF e compreender as recomendações de fluxo geradas na tela em menos de 2 minutos no primeiro acesso, sem a necessidade de suporte ou tutoriais externos. |
| **H2** | Usabilidade | Proteção contra Erros do Usuário | Estima-se que os mecanismos de validação da interface barrem e tratem corretamente pelo menos 95% das tentativas de envio de arquivos corrompidos ou em formatos inválidos (diferentes do PDF padrão emitido pelo SIGAA). |
| **H3** | Usabilidade | Acessibilidade | Acredita-se que os elementos críticos de interação (como os botões de upload e os nós do grafo de disciplinas) cumpram os critérios básicos de contraste visual e navegação por teclado, permitindo a operação da plataforma por estudantes com limitações visuais sem bloqueios na interface. |
| **H4** | Usabilidade | Reconhecimento da Adequação | Estima-se que mais de 80% dos usuários consigam identificar imediatamente, logo na tela inicial, se a plataforma possui as funcionalidades adequadas para resolver suas dúvidas sobre o fluxo de disciplinas do seu curso. |
| **H5** | Eficiência de Desempenho | Comportamento em Relação ao Tempo | Sob condições normais e estáveis de infraestrutura de rede, o tempo médio gasto entre o upload do histórico do SIGAA, o processamento interno da aplicação e a renderização completa do grafo na tela não deve ultrapassar 4 segundos. |
| **H6** | Eficiência de Desempenho | Fator de Variação Externa (Latência) | Espera-se que a oscilação no tempo de resposta da API externa do assistente Darcy AI (Maritaca AI) atue como o principal fator de variação de desempenho, podendo degradar o tempo de resposta do sistema em até 50% em momentos de instabilidade do servidor deles. |
| **H7** | Eficiência de Desempenho | Fator de Variação de Carga (Concorrência) | Estima-se que cenários simulados de uso simultâneo (simulando os períodos críticos de matrícula na UnB) aumentem o tempo de resposta da leitura sequencial de arquivos em até 40% em comparação com acessos isolados. |

<center><sub>Tabela 3 — Hipóteses de linha de base.</sub></center>

## Justificativas

Fundamentado nos impactos práticos e na necessidade de validar se a "dor do estudante" está sendo efetivamente mitigada pela plataforma, conforme estabelecido em [Escopo, Profundidade e Objetos de Avaliação](../fase_1_v2/escopo.md):

| Objetivo | Relevância para o Ecossistema | Impacto Prático e Tomada de Decisão |
| :--- | :--- | :--- |
| **Objetivo 1:<br>Usabilidade** | O sistema foca em reduzir a carga cognitiva na montagem da grade. Se a interface (grafos, fluxo, upload) for confusa, o sistema falha em seu propósito principal de engajamento do estudante. | Os resultados permitirão identificar se a navegação visual do "Meu Fluxograma" é intuitiva ou se gera atrito, permitindo ajustes de interface que facilitem a autonomia do aluno sem necessidade de tutoriais. |
| **Objetivo 2:<br>Eficiência** | O desempenho é crítico devido à natureza das integrações (leitura de PDF do SIGAA e chamadas de API com a Maritaca AI). A latência nesses processos é a principal fonte de frustração em um sistema focado em produtividade acadêmica. | As medições nortearão melhorias na percepção de fluidez. Mesmo sem acesso ao código (caixa-preta), entender o tempo de resposta do "Darcy AI" ajudará a alinhar as expectativas do usuário e a otimizar o fluxo de importação. |

<center><sub>Tabela 4 — Justificativas dos objetivos de medição.</sub></center>

---


## Referências

<a id="ref01"></a>[1] RAMOS, Cristiane Soares. **Medição baseada em objetivos — Goal-Question-Metric (GQM)**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025. Material de aula da disciplina FGA0278 — Qualidade de Software 1. Baseado no material da Profa. Dra. Káthia Marçal Oliveira. Disponível em: [slide_gqm.pdf](../assets/referencia/slide_gqm.pdf).

<a id="ref02"></a>[2] BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, H. Dieter. **Goal Question Metric Paradigm**. In: MARCINIAK, John J. (Ed.). *Encyclopedia of Software Engineering*. 2. ed. New York: Wiley, 2002. (Abordagem GQM definida originalmente em 1994.)

<a id="ref03"></a>[3] INTERNATIONAL ORGANIZATION FOR STANDARDIZATION (ISO). **ISO/IEC 25000:2014 — Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — Guide to SQuaRE**. Geneva: ISO, 2014. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards>.

## Declaração do uso de IA

Eu, [Camila Careli](https://github.com/camilascareli), declaro que utilizei a ferramenta CursorIA para fins de organização do mkdocs.

## Histórico de Versão

| Versão | Data | Descrição | Autor |
|---|---|---|---|
| 1.0 | 06/06/26 | Escrita do conteúdo do documento | Camila Careli |
| 1.1 | 06/06/26 | Apenas adicionei tags de hiperlink para usar nas questões GQM | Ana Luiza |