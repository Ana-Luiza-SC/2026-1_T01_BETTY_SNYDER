# Requisitos de Avaliação

## 1. Identificação do Produto

A etapa de identificação do produto é o ponto de partida da avaliação. Ela visa registrar formalmente o software avaliado, sua versão, domínio de aplicação e os objetivos que motivam a avaliação, de forma que qualquer leitor compreenda exatamente o que está sendo analisado e por quê. A tabela 1 apresenta um resumo sobre o software avaliado. Mais infromações sobre a categorização podem ser encontradas na aba de [categorização](categoria.md).

| Campo | Informação |
| ----- | ---------- |
| **Nome do produto** | No Fluxo UNB |
| **URL** | https://no-fluxo.crianex.com/ |
| **Tipo de sistema** | Aplicação web responsiva |
| **Plataforma** | Web (navegador), responsivo para dispositivos móveis e desktop |
| **Domínio da aplicação** | Educacional e Acadêmico — planejamento e gestão de grade curricular universitária |
| **Público-alvo** | Estudantes de graduação da Universidade de Brasília (UnB) |
| **Versão avaliada** | Versão disponível em produção (mai/2026) |

_Figura 1 — Categorização do No Fluxo UNB._

### 1.1 Domínio da Aplicação

O No Fluxo UNB está inserido no domínio **Educacional e Acadêmico**, atuando especificamente no nicho de planejamento e gestão de grade curricular universitária. O sistema foi desenvolvido para resolver um problema concreto e frequente entre estudantes da UnB: a dificuldade em compreender o fluxo de disciplinas do próprio curso, identificar pré-requisitos e equivalências, e planejar semestralmente a matrícula de forma consciente. Mais informações sobre a descrição do projeto podem ser encontradas na aba de [descrição](descricao.md).

### 1.2 Objetivo em Relação à Avaliação

A avaliação do No Fluxo UNB tem como objetivo verificar se o sistema atende aos requisitos de qualidade relacionados à **Usabilidade** e à **Eficiência de Desempenho**, considerando seu contexto de utilização por estudantes da Universidade de Brasília (UnB). A avaliação seguirá diretrizes da série SQuaRE (ISO/IEC 25000) e utilizará evidências para apoiar decisões de melhoria.

De forma mais específica, a avaliação busca:

- Identificar problemas de navegação, interação e compreensão nas funcionalidades principais do sistema;
- Avaliar a eficiência do processamento de dados em operações críticas, como upload de histórico, leitura de regras acadêmicas e renderização do fluxograma;
- Verificar a confiabilidade e o tempo de resposta do Assistente Darcy AI e de integrações externas como o SIGAA;
- Gerar insumos concretos para que a equipe de desenvolvimento priorize melhorias de usabilidade e desempenho.

---

## 2. Análise de Requisitos de Qualidade

A análise de requisitos de qualidade visa definir, de forma estruturada, **o que** deve ser avaliado no produto e **com que profundidade**, partindo dos objetivos da avaliação que traduzem diretamente o interesse do requisitante.

Ela define:

- A **profundidade** da avaliação — o nível de detalhe com que cada característica será investigada;
- A **abrangência** — quais módulos e funcionalidades entram no escopo;
- O **relacionamento** da presente avaliação com avaliações anteriores ou futuras, quando aplicável;
- Os **objetos de avaliação** — os elementos concretos do sistema sobre os quais serão aplicadas as medições.

### 2.1 Aspectos de Qualidade e Ênfase

As características de **Usabilidade** e **Eficiência de Desempenho** foram priorizadas com ênfase máxima por serem as mais diretamente vinculadas ao propósito declarado da avaliação e ao contexto de uso do público-alvo. Mais informações sobre a priorização das características selecionadas podem ser encontradas na página [características](caracteristicas.md).

### 2.2 Abrangência, Profundidade e Objetos de Avaliação

**Abrangência:** A avaliação cobre os módulos principais do sistema acessíveis em produção, com foco nas funcionalidades de maior impacto na experiência do usuário e na integridade dos dados:

- **Módulo Meu Fluxograma** — núcleo da experiência, renderização gráfica do fluxo acadêmico, visualização de pré-requisitos, equivalências e status das disciplinas;
- **Módulo de Importação de Histórico (Upload/SIGAA)** — principal porta de entrada de dados do sistema, incluindo leitura de histórico em PDF e integração com o SIGAA;
- **Módulo de Seleção de Curso** — definição do curso ou habilitação cujo fluxograma será analisado;
- **Módulo de Disciplinas** — consulta de pré-requisitos, cadeias topológicas e informações detalhadas de cadeira;
- **Assistente Darcy AI** — agente de IA para suporte ao usuário, com foco na confiabilidade das respostas e no tempo de resposta de integrações externas.

**Profundidade:** A avaliação combina inspeção heurística da interface, verificação de comportamento nos fluxos principais de uso e medições objetivas de tempo de resposta. Não serão realizados testes extensivos de carga, segurança avançada ou análise interna da infraestrutura de rede.

**Objetos de avaliação:**

| Objeto | Aspecto avaliado |
| ------ | ---------------- |
| Upload e leitura de histórico escolar | Usabilidade e eficiência (tempo de processamento, tratamento de erros e feedback ao usuário) |
| Seleção de curso e definição do fluxograma | Usabilidade (clareza do fluxo e consistência da experiência) |
| Renderização do fluxograma interativo | Usabilidade e eficiência (tempo de carregamento, legibilidade e organização por status) |
| Consulta de pré-requisitos e equivalências | Usabilidade (compreensão das dependências e acesso à informação) |
| Assistente Darcy AI | Eficiência e confiabilidade (tempo de resposta e comportamento em integrações externas) |

**Relacionamento com avaliações anteriores/futuras:** Esta é a avaliação inicial do produto no contexto da disciplina. Os resultados desta fase servirão de linha de base para avaliações futuras e orientarão o ciclo de melhorias da equipe de desenvolvimento.

**Tópicos que estão fora do escopo dessa avaliação:**

- Qualidade dos dados provenientes do SIGAA (sistema externo à equipe);
- Segurança da integração com o SIGAA (depende de infraestrutura da UnB);
- Qualidade intrínseca do modelo de IA da Maritaca (componente de terceiro);
- Testes extensivos de carga e estresse;
- Avaliações profundas de infraestrutura de rede e servidores.

---

## 3. Critérios de Sucesso da Avaliação
 
Esta seção define o que significa, de forma objetiva, que a avaliação foi bem-sucedida. Estabelecer esses critérios previamente evita avaliações vagas e garante que os resultados sejam úteis para a tomada de decisão pela equipe.
 
### 3.1 Métricas Principais
 
A avaliação será considerada bem-sucedida se atender aos seguintes critérios:
 
1. **Cobertura funcional**: Avaliar no mínimo 80% dos módulos críticos identificados no escopo — Meu Fluxograma, Importação de Histórico, Seleção de Curso, Módulo de Disciplinas e Assistente Darcy AI.
2. **Participação de usuários**: Realizar testes com pelo menos 3 participantes representativos do público-alvo (estudantes de graduação da UnB), de preferência de cursos e semestres distintos para cobrir perfis variados de histórico acadêmico.
3. **Identificação de problemas**: Encontrar e documentar no mínimo 3 problemas de usabilidade ou eficiência com severidade moderada ou alta, com evidências reproduzíveis.
4. **Mensuração de desempenho**: Registrar tempos de resposta para ao menos 3 operações (renderização do fluxograma, processamento do upload de histórico e resposta do assistente Darcy AI), com base em condições reais de uso.
5. **Proposição de melhorias**: Para cada problema identificado, sugerir ao menos uma melhoria concreta e viável.

### 3.2 Resultados Esperados
 
Ao final da avaliação, espera-se entregar:
 
- Relatório detalhado com os problemas encontrados, priorizados por severidade e impacto no usuário;
- Recomendações específicas de melhoria, organizadas por módulo e característica de qualidade afetada (usabilidade ou eficiência);
- Registro das medições de desempenho coletadas;
- Base documental para orientar as próximas fases da avaliação e as iterações de desenvolvimento do sistema.

---

## Histórico de versão

| Versão | Data | Descrição | Autor |
|---|---|---|---|
| 1.0 | 03/06/26 | Criação da página | Ígor Veras |
| 1.1 | 03/06/26 | Elaboração do conteúdo completo | Ígor Veras |
| 1.2 | 05/06/26 | Adequação da página com descrição e objetivos novos | Ígor Veras |
