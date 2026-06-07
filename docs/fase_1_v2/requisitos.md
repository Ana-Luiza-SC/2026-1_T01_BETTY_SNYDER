# Requisitos de Avaliação

## 1. Identificação do Produto

A identificação do produto formaliza os dados básicos do software avaliado, permitindo que qualquer leitora ou leitor compreenda o contexto, a finalidade e o escopo deste trabalho. Informações complementares sobre o software — incluindo suas funcionalidades, ambiente de uso e perfil de usuários — estão disponíveis na página de [Descrição do Software](descricao.md).

| Campo | Informação |
| :--- | :--- |
| **Nome do produto** | No Fluxo UNB |
| **URL** | https://no-fluxo.crianex.com/ |
| **Tipo de sistema** | Aplicação web responsiva |
| **Plataforma** | Web (navegador), responsivo para dispositivos móveis e desktop |
| **Domínio da aplicação** | Educacional e Acadêmico — planejamento e gestão de grade curricular universitária |
| **Público-alvo** | Estudantes de graduação da Universidade de Brasília (UnB) |
| **Versão avaliada** | Versão disponível em produção (mai/2026) |

<center><sub>Tabela 1 — Identificação básica do produto avaliado.</sub></center>

### 1.1 Domínio da Aplicação

O No Fluxo UNB pertence ao domínio **Educacional e Acadêmico**, atuando como ferramenta de apoio ao planejamento e à gestão de trajetórias curriculares da UnB. O sistema foi concebido para reduzir a complexidade da leitura de históricos escolares, pré-requisitos e equivalências, ajudando estudantes a planejar suas matrículas de forma mais assertiva.

A classificação detalhada do software segundo as taxonomias de Pressman, IEEE 1062 e ISO/IEC 25010 está documentada na página de [Categorias do Software](categoria.md). Mais informações sobre o produto, suas funcionalidades, tarefas e ambiente de uso podem ser encontradas na página de [Descrição](descricao.md).

### 1.2 Objetivo e Propósito da Avaliação

O propósito desta avaliação está inserido no contexto da disciplina de Qualidade de Software (FGA0278), ministrada pela professora Cristiane Soares Ramos, com o objetivo de aplicar em um produto real os conceitos e práticas definidos pela série de normas ISO/IEC 25000 (SQuaRE). A motivação completa para a realização da avaliação, bem como as partes interessadas e o uso pretendido dos resultados, estão descritos na página de [Propósito da Avaliação](proposito_avaliacao.md) e de [Objetivo da Avaliação](objetivo_avaliacao.md).

O objetivo desta avaliação é verificar se o No Fluxo UNB atende aos requisitos de qualidade de software relacionados à **Usabilidade** e à **Eficiência de Desempenho**, com base nas diretrizes da série SQuaRE (ISO/IEC 25000), adotando uma abordagem de caixa-preta sobre o sistema disponível em produção.

Os objetivos específicos da avaliação são:

- Identificar lacunas de usabilidade nos fluxos de navegação, visualização de fluxogramas e importação de históricos;
- Avaliar o desempenho do processamento de dados nos principais pontos críticos do sistema;
- Verificar o tempo de resposta e a confiabilidade do Assistente Darcy AI e de integrações externas como o SIGAA;
- Produzir recomendações de melhoria que suportem decisões futuras de priorização da equipe de desenvolvimento.

---

## 2. Análise de Requisitos de Qualidade

Esta seção define os requisitos de qualidade que orientam o trabalho, indicando o que será avaliado, com que profundidade e em quais objetos do sistema.

### 2.1 Aspectos de Qualidade e Ênfase

Foram selecionadas as características de qualidade de **Usabilidade** e **Eficiência de Desempenho** como foco principal da avaliação. Essa escolha foi motivada pelo impacto direto que ambas exercem na experiência dos estudantes durante o uso da plataforma — o sistema é utilizado diretamente por alunos que dependem de uma interface intuitiva e de respostas rápidas para planejar sua vida acadêmica.

A tabela abaixo apresenta a ênfase atribuída a cada característica de qualidade, seguindo a escala de 1 (nenhum interesse) a 5 (grande interesse) definida no processo de avaliação de produto de software [[3]](#ref03). A definição completa das características, suas subcaracterísticas e justificativas de seleção estão documentadas na página de [Características de Qualidade Selecionadas](caracteristicas.md).

| Característica | Ênfase | Justificativa |
| :--- | :---: | :--- |
| **Usabilidade** | 5 | O sistema é utilizado diretamente por estudantes, exigindo uma interface intuitiva, de fácil aprendizado e compreensão. |
| **Eficiência de Desempenho** | 5 | O processamento dos históricos acadêmicos e a geração dos fluxogramas devem ocorrer de forma rápida, garantindo uma experiência satisfatória aos usuários. |
| **Funcionalidade** | 3 | Embora importante, a avaliação não possui foco na validação funcional completa do sistema nesta etapa. |
| **Confiabilidade** | 2 | Não constitui o principal objetivo da avaliação atual. |
| **Completitude** | 2 | Não constitui o principal objetivo da avaliação atual. |
| **Portabilidade** | 1 | Não faz parte do escopo definido para esta avaliação. |

<center><sub>Tabela 2 — Ênfase atribuída às características de qualidade do produto (reproduzida de <a href="caracteristicas.md">Características</a>).</sub></center>

As subcaracterísticas de **Usabilidade** priorizadas nesta avaliação são: Reconhecimento da Adequação, Capacidade de Aprendizado, Proteção contra Erros do Usuário e Acessibilidade. Para **Eficiência de Desempenho**, as subcaracterísticas em foco são: Comportamento em Relação ao Tempo e Capacidade. O detalhamento de cada subcaracterística, seu impacto e risco associado estão descritos em [Características de Qualidade Selecionadas](caracteristicas.md).

### 2.2 Abrangência e Profundidade

**Abrangência:** A avaliação abrange os módulos mais relevantes para a experiência do usuário e para a integridade dos dados. A definição do escopo seguiu quatro critérios práticos — foco na dor do estudante, avaliação centrada no produto (caixa-preta), esforço concentrado e transparência nas exclusões —, conforme detalhado na página de [Escopo, Profundidade e Objetos de Avaliação](escopo.md). Os módulos contemplados são:

- **Meu Fluxograma:** visualização gráfica do fluxo acadêmico, pré-requisitos, equivalências e status das disciplinas;
- **Importação de Histórico (Upload/SIGAA):** entrada de dados por arquivo PDF ou integração externa;
- **Seleção de Curso:** definição do currículo e da habilitação analisada;
- **Módulo de Disciplinas:** consulta de pré-requisitos, cadeia de dependências e informações detalhadas;
- **Assistente Darcy AI:** suporte em linguagem natural, com foco em tempo de resposta e confiabilidade.

**Profundidade:** A investigação combinará análise heurística da interface, inspeção de fluxos principais e coleta de métricas de desempenho perceptíveis. Não serão realizadas análises de carga em larga escala nem auditorias de segurança ou de infraestrutura interna. Os limites de validade das conclusões e os aspectos intencionalmente excluídos desta etapa estão registrados na página de [Escopo](escopo.md).

### 2.3 Objetos de Avaliação

Os objetos de avaliação são componentes concretos do sistema que serão analisados quanto às características de qualidade definidas. A tabela abaixo estabelece os objetos de medição e os aspectos avaliados em cada um, relacionando-os às características de Usabilidade e Eficiência de Desempenho selecionadas na seção 2.1.

| Objeto | Aspecto avaliado |
| :--- | :--- |
| Upload e leitura de histórico escolar | Usabilidade e eficiência (tempo de processamento, tratamento de erros e feedback ao usuário) |
| Seleção de curso e definição do fluxograma | Usabilidade (clareza do fluxo e consistência da experiência) |
| Renderização do fluxograma interativo | Usabilidade e eficiência (tempo de carregamento e legibilidade visual do grafo) |
| Consulta de pré-requisitos e equivalências | Usabilidade (compreensão das dependências e acesso à informação) |
| Assistente Darcy AI | Eficiência e confiabilidade (tempo de resposta e comportamento em integrações externas) |

<center><sub>Tabela 3 — Objetos de avaliação e aspectos de qualidade mensurados.</sub></center>

**Relação com avaliações anteriores/futuras:** Esta é a avaliação inicial do produto no contexto da disciplina. Conforme descrito na seção de [Escopo](escopo.md), os dados colhidos aqui funcionarão como uma **linha de base (*baseline*)** — ponto de partida documentado para que futuras melhorias possam ser comparadas e medidas objetivamente.

**Fora do escopo desta avaliação:**

- Qualidade dos dados fornecidos pelo SIGAA;
- Segurança da integração com o SIGAA;
- Avaliação do modelo de IA da Maritaca;
- Testes extensivos de estresse e carga;
- Análise interna de rede ou infraestrutura de servidores.

---

## 3. Critérios de Sucesso da Avaliação

Esta seção define critérios objetivos que indicam se a avaliação cumpriu seu propósito de produzir resultados úteis e aplicáveis. Os critérios abaixo foram estabelecidos com base nos objetivos descritos na página de [Objetivo da Avaliação](objetivo_avaliacao.md) e no alinhamento com as características de qualidade selecionadas em [Características](caracteristicas.md).

### 3.1 Métricas Principais

A avaliação será considerada bem-sucedida se atender aos seguintes critérios:

1. **Cobertura funcional:** avaliar no mínimo 80% dos módulos críticos definidos no escopo;
2. **Participação de usuários:** envolver ao menos 3 estudantes de graduação da UnB, de cursos e semestres variados;
3. **Identificação de problemas:** documentar pelo menos 3 problemas de usabilidade ou eficiência com severidade moderada ou alta;
4. **Mensuração de desempenho:** registrar tempos de resposta de pelo menos 3 operações críticas;
5. **Proposição de melhorias:** sugerir ao menos uma melhoria concreta para cada problema identificado.

### 3.2 Resultados Esperados

Ao final da avaliação, espera-se entregar:

- Relatório com problemas encontrados e priorizados por severidade;
- Recomendações de melhoria por módulo e característica de qualidade;
- Registro das medições de desempenho coletadas;
- Base documental para orientar fases futuras da avaliação.

---

## Referências

<a id="ref01"></a>INTERNATIONAL ORGANIZATION FOR STANDARDIZATION (ISO). **ISO/IEC 25000:2014 - Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE)**. Geneva: ISO, 2014.

<a id="ref02"></a>NO FLUXO UNB. **Plataforma de acompanhamento e planejamento de fluxo acadêmico**. Versão 1.0. Brasília: Crianex, 2026.

<a id="ref03"></a>RAMOS, Cristiane Soares. **Processo de Avaliação de Produto de Software**. Brasília: Universidade de Brasília, Faculdade do Gama, 2026. Material de aula da disciplina FGA0278 - Qualidade de Software.

## Declaração do uso de IA

Eu, [Ígor Veras](https://github.com/igorv), declaro que utilizei uma ferramenta de IA para estruturar e organizar o conteúdo deste arquivo em conformidade com o estilo dos demais documentos.

## Histórico de versão

| Versão | Data | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| 1.0 | 03/06/26 | Criação da página | Ígor Veras |
| 1.1 | 03/06/26 | Elaboração do conteúdo completo | Ígor Veras |
| 1.2 | 05/06/26 | Alinhamento do formato ao padrão dos demais arquivos | Ígor Veras |
| 1.3 | 07/06/26 | Integração de referências cruzadas, contextualização das tabelas e alinhamento com demais documentos | Ígor Veras |