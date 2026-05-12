# Fase 1 - Requisitos de avaliação

## Contexto do trabalho

Este trabalho foi desenvolvido no âmbito da disciplina de Qualidade de Software, para definir os requisitos de avaliação da qualidade do
software escolhido pela equipe, o [No Fluxo UNB](https://no-fluxo.crianex.com/), incluindo:

1. Propósito da avaliação;
2. Identificação do tipo de produto;
3. Especificação inicial do modelo de qualidade.

## Sobre o aplicativo

O [No Fluxo UNB](https://no-fluxo.crianex.com/) é um sistema web desenvolvido para auxiliar estudantes da Universidade de Brasília no planejamento acadêmico do curso. O software oferece um fluxograma interativo e personalizado, permitindo que os alunos organizem melhor sua trajetória universitária.

O principal problema que o sistema busca resolver é a dificuldade dos estudantes em entender o fluxo das disciplinas e identificar pré-requisitos e equivalências, logo se faz muito necessário seu aperfeiçoamento devido à sua importância.

## Propósito da Avaliação e Uso Pretendido

A avaliação da qualidade do software No Fluxo UNB tem como propósito verificar se o sistema atende aos requisitos de qualidade relacionados à usabilidade e à eficiência de desempenho, considerando seu contexto de utilização por estudantes da Universidade de Brasília (UnB).

A avaliação será utilizada como apoio à tomada de decisões pela equipe do projeto, em especial para:

- Identificar problemas de navegação e interação na interface;
- Definir melhorias de desempenho em funcionalidades críticas;
- Melhorar a satisfação e a produtividade dos usuários finais.

Os principais usuários dos resultados da avaliação serão:

| Parte                      | Uso dos Resultados                                               |
| -------------------------- | ---------------------------------------------------------------- |
| Desenvolvedores            | Corrigir problemas de interface, desempenho e fluxo de navegação |
| Equipe de qualidade        | Priorizar testes e validar requisitos de qualidade               |
| Administradores do sistema | Monitorar estabilidade e comportamento operacional               |
| Coordenação do projeto     | Apoiar decisões sobre evolução e priorização de melhorias        |
| Usuários finais            | Beneficiados indiretamente pelas melhorias implementadas         |

O cenário de aplicação da avaliação envolve o uso real do sistema web por estudantes em atividades cotidianas, considerando:

- Navegação em diferentes dispositivos;
- Execução simultânea de acessos;
- Uso contínuo das funcionalidades principais;
- Necessidade de respostas rápidas e interface intuitiva.
  Dessa forma, os resultados da avaliação serão usados diretamente para orientar decisões técnicas e gerenciais sobre a evolução do sistema, garantindo maior qualidade de uso e desempenho.

## Descrição Estruturada e Classificação do Software

### Identificação do Produto

| Campo               | Informação                                                     |
| ------------------- | -------------------------------------------------------------- |
| **Nome**            | No Fluxo UNB                                                   |
| **URL**             | https://no-fluxo.crianex.com/                                  |
| **Tipo de sistema** | Aplicação web (SPA — Single Page Application)                  |
| **Plataforma**      | Web (navegador), responsivo para dispositivos móveis e desktop |
| **Domínio**         | Planejamento acadêmico universitário                           |
| **Público-alvo**    | Estudantes de graduação da Universidade de Brasília (UnB)      |
| **Versão avaliada** | Versão disponível em produção (mai/2026)                       |

### Classificação do Tipo de Produto

De acordo com a norma ISO/IEC 25010 (SQuaRE), o **No Fluxo UNB** é classificado como:

- **Produto de software de uso direto por usuário final** — sistema interativo baseado em navegador, acessado diretamente por estudantes sem instalação local.
- **Categoria**: Sistema de informação / ferramenta de apoio à decisão acadêmica.
- **Modo de operação**: Online, com acesso autenticado (funcionalidades completas) e não autenticado (consulta pública de fluxogramas).

Essa classificação implica que características como **eficiência de desempenho**, **compatibilidade**, **segurança** e **confiabilidade** são especialmente relevantes para a avaliação, dado o contexto de uso real em ambiente web com múltiplos acessos simultâneos.

### Descrição Estruturada do Software

### Visão Geral

O No Fluxo UNB é um sistema web desenvolvido para auxiliar estudantes da Universidade de Brasília no planejamento de sua trajetória acadêmica. A plataforma oferece fluxogramas interativos e personalizados por curso, com integração ao histórico acadêmico do SIGAA e assistente de inteligência artificial.

O problema central resolvido pelo sistema é a dificuldade dos estudantes em visualizar e compreender o fluxo de disciplinas, identificar pré-requisitos, equivalências e planejar semestralmente suas matrículas.

##### Tela Inicial (Home)

![Tela inicial do No Fluxo UNB](../assets/fase1/home.png)

_Figura 1 — Tela inicial do sistema. Apresenta as duas modalidades de acesso: consulta como visitante (sem cadastro) e recursos exclusivos com login._

A página inicial apresenta claramente o propósito da plataforma, com dois caminhos de acesso distintos: consulta livre de fluxogramas (visitante) e recursos personalizados que exigem autenticação (upload de histórico, salvamento de progresso e sugestões por IA).

##### Módulos Principais

##### 1. Módulo de Fluxogramas

![Lista de fluxogramas disponíveis](../assets/fase1/lista-fluxogramas.png)

_Figura 2 — Listagem dos fluxogramas disponíveis. Exibe 518 cursos cadastrados com filtros por nome, tipo e turno._

Permite explorar e selecionar o fluxograma de qualquer curso da UnB. Possui busca por nome, tipo (ex.: Bacharelado, Licenciatura) e turno (Diurno/Noturno), além de paginação. Disponível para visitantes não autenticados.

##### 2. Módulo Meu Fluxograma (Visão Grade)

![Fluxograma pessoal — visão grade](../assets/fase1/meu-fluxo.png)

_Figura 3 — Visão em grade do fluxograma pessoal (curso de Engenharia de Software). Exibe disciplinas por semestre com codificação visual por status: aprovado (verde), matriculado (roxo), disponível (laranja), reprovado (vermelho) e bloqueado (cinza)._

Exibe o fluxograma personalizado do estudante com:

- Organização por semestre (1º ao 10º);
- Indicação de carga horária integralizada por semestre;
- Codificação por cores representando o status de cada disciplina;
- Acesso rápido a optativas e assistente de IA;
- Controles de zoom e modos de exibição de dependências (Diretas / Todas / Off).

##### 3. Módulo Meu Fluxograma (Visão com Linhas de Dependência)

![Fluxograma com todas as linhas de dependência](../assets/fase1/fluxo-com-todas-linhas.png)

_Figura 4 — Visão do fluxograma com linhas de pré-requisito ativas (modo "Todas"). As setas coloridas conectam disciplinas e representam as cadeias de dependência entre elas._

Complementa a visão em grade ao ativar as linhas de pré-requisitos e equivalências entre disciplinas, permitindo ao estudante entender visualmente quais matérias desbloqueiam outras ao longo do curso.

##### 4. Módulo Meu Fluxograma — Painel de Progresso e Ferramentas

![Painel de progresso e ferramentas](../assets/fase1/meu-fluxo2.png)

_Figura 5 — Painel inferior do fluxograma pessoal. Exibe carga horária integralizada (64%), semestre atual (7º), IRA e ferramenta de simulação de mudança de curso._

Exibe ao estudante:

- Percentual de carga horária integralizada (via SIGAA);
- Semestre atual e projeção para o próximo semestre;
- IRA (Índice de Rendimento Acadêmico);
- Ferramenta de simulação de mudança de curso.

##### 5. Módulo de Outros Fluxogramas (modo comparação)

![Outros fluxogramas — modo visualização externa](../assets/fase1/outros-fluxogramas.png)

_Figura 6 — Fluxograma de outro curso (Administração, Bacharelado Diurno 2018.2) acessado a partir da lista pública. Permite visualizar fluxogramas de outros cursos com a mesma interface._

Ao selecionar um fluxograma diferente do seu, o estudante pode visualizar o currículo completo de outro curso com controles de zoom, troca de matriz e botão de retorno ao seu fluxograma pessoal.

##### 6. Módulo de Disciplinas

![Tela de disciplinas com busca e cadeia topológica](../assets/fase1/lista-disciplinas.png)

_Figura 7 — Módulo de Disciplinas. Exibe a cadeia topológica de pré-requisitos e dependentes de uma disciplina selecionada (exemplo: Engenharia de Software — CIC0105)._

Permite buscar qualquer disciplina da UnB pelo nome ou código e visualizar:

- Pré-requisitos diretos da disciplina;
- Disciplinas que dependem dela (dependentes);
- Representação em grafo da cadeia topológica completa.

##### 7. Módulo Assistente (Darcy AI)

![Assistente virtual Darcy AI](../assets/fase1/assistente-virtual.png)

_Figura 8 — Assistente virtual Darcy AI, alimentado pela plataforma Maritaca AI. Oferece sugestões de matérias, responde dúvidas e permite perguntas livres relacionadas ao curso._

Assistente conversacional integrado à plataforma, com sugestões rápidas (ex.: "Recomendar matérias do meu curso") e campo de texto livre. Permite que o estudante obtenha orientações sobre disciplinas e planejamento acadêmico com suporte de IA.

##### 8. Módulo de Importação de Histórico (Upload SIGAA)

![Tela de upload do histórico acadêmico](../assets/fase1/up-load-historico.png)

_Figura 9 — Tela de importação de histórico acadêmico. O estudante faz upload do PDF oficial emitido pelo SIGAA (máx. 10 MB) para que o sistema popule automaticamente seu fluxograma._

Permite ao estudante autenticado importar o histórico acadêmico em PDF (emitido pelo SIGAA) para que o sistema identifique automaticamente as disciplinas cursadas, aprovadas, reprovadas ou em andamento.

##### 9. Integração com o SIGAA

![Modal de integração com autenticação SIGAA](../assets/fase1/integracao-sigaa.png)

_Figura 10 — Modal de autenticação integrada com o SIGAA. O estudante insere suas credenciais institucionais para obtenção automática do histórico acadêmico._

O sistema oferece integração via autenticação com o SIGAA (Sistema Integrado de Gestão de Atividades Acadêmicas da UnB), permitindo que o histórico do estudante seja obtido automaticamente sem necessidade de exportação manual do PDF.

#### Dependências e Integrações Externas

| Componente        | Papel no sistema                                                                              |
| ----------------- | --------------------------------------------------------------------------------------------- |
| **SIGAA (UnB)**   | Fonte de dados do histórico acadêmico do estudante (via upload PDF ou autenticação integrada) |
| **Maritaca AI**   | Provedor do modelo de IA que alimenta o assistente Darcy AI                                   |
| **Navegador web** | Ambiente de execução; compatibilidade com Chrome, Firefox, Edge e Safari esperada             |

#### Restrições e Limitações Conhecidas

- O sistema depende de dados fornecidos pelo SIGAA; inconsistências no histórico acadêmico podem impactar a precisão do fluxograma exibido.
- Funcionalidades personalizadas (fluxograma próprio, assistente, carga horária integralizada) requerem autenticação.
- O upload de histórico está limitado a arquivos PDF de até 10 MB emitidos oficialmente pela UnB.
- A cobertura de cursos e matrizes depende da atualização contínua da base de dados da plataforma.

### Implicações para a Avaliação

A descrição estruturada acima evidencia os seguintes pontos relevantes para o escopo da avaliação:

- **O que é possível medir agora**: eficiência de desempenho no carregamento dos fluxogramas, comportamento sob múltiplos acessos, tempo de resposta do assistente de IA, usabilidade percebida da interface de navegação.
- **O que está fora do escopo imediato**: qualidade dos dados provenientes do SIGAA (fora do controle da equipe), segurança da integração SIGAA (depende de infraestrutura externa), e a qualidade do modelo de IA da Maritaca.
- **Módulos críticos para a avaliação**: Meu Fluxograma (núcleo da experiência do usuário), Importação de Histórico (funcionalidade de alto impacto e dependência externa) e Assistente Darcy AI (componente de IA com comportamento não-determinístico).

### Tabela de versão

| Versão | Autor          | Data       | Descrição                                        |
| ------ | -------------- | ---------- | ------------------------------------------------ |
| 1.0    | Julia Gabriela | 11/05/2026 | Criação do documento.                            |
| 1.1    | Ana Luiza      | 12/05/2026 | Adição da Descrição Estruturada e Classificação. |
