# Objetivo da Avaliação 

## Sobre o Aplicativo

O [No Fluxo UNB](https://no-fluxo.crianex.com/) é um sistema web desenvolvido  por estudantes da Faculdade de Ciência e Tecnologia(FCTE), no âmbito da disciplina de Metodologia e Desenvolvimento de Software, visando auxiliar estudantes da Universidade de Brasília no planejamento acadêmico do curso. O software oferece um fluxograma interativo e personalizado, permitindo que os alunos organizem melhor sua trajetória universitária.

O principal problema que o sistema busca resolver é a dificuldade dos estudantes em entender o fluxo das disciplinas e identificar pré-requisitos e equivalências, logo se faz muito necessário seu aperfeiçoamento devido à sua importância.

## Domínio da Aplicação

O sistema está inserido no domínio Educacional e Acadêmico. Ele atua especificamente no nicho de planejamento e gestão de grade curricular. O seu principal objetivo é solucionar a dificuldade frequente dos estudantes em compreender o fluxo de disciplinas de seus cursos, bem como identificar facilmente os pré-requisitos e equivalências exigidos pela universidade. 

## Funcionalidades do Sistema (Escopo da Avaliação) 

Para cumprir seu propósito, o sistema conta com fluxos essenciais de interação e processamento de dados, destacando-se:

- Upload e Leitura de Dados: Permite que o aluno faça o upload do seu histórico escolar em formato específico.
- Seleção de Curso: Interface para que o usuário defina ou confirme qual o fluxograma (curso/habilitação) deseja analisar.
- Processamento de Regras: Motor interno que cruza as informações do histórico com as regras da UnB (pré-requisitos, co-requisitos e equivalências).
- Renderização de Fluxograma Interativo: Geração de uma interface gráfica (dashboard/fluxograma) que classifica as disciplinas por status (cursadas, a cursar, trancadas) e as organiza por semestre.

## Propósito da Avaliação e Uso Pretendido

A avaliação da qualidade do software No Fluxo UNB tem como propósito verificar se o sistema atende aos requisitos de qualidade relacionados à usabilidade e à eficiência de desempenho, considerando seu contexto de utilização por estudantes da Universidade de Brasília (UnB).

A avaliação será utilizada como apoio à tomada de decisões pela equipe do projeto, em especial para:

- Identificar problemas de navegação e interação na interface;
- Definir melhorias de desempenho em funcionalidades críticas;
- Melhorar a satisfação e a produtividade dos usuários finais.
- Os principais usuários dos resultados da avaliação serão:

Os resultados da avaliação serão utilizados por diferentes partes interessadas do projeto **No Fluxo UnB**, servindo como base para decisões técnicas e gerenciais relacionadas à qualidade do sistema. Para a equipe de desenvolvimento, os resultados fornecerão informações objetivas sobre problemas de interface, desempenho e fluxo de navegação, permitindo identificar defeitos, corrigir inconsistências e implementar melhorias que aumentem a eficiência e a experiência dos usuários.

A equipe de qualidade utilizará os dados obtidos para verificar o atendimento aos requisitos de qualidade definidos para o sistema, além de apoiar a priorização de atividades de teste e validação. Dessa forma, será possível direcionar esforços para as áreas que apresentam maior risco ou impacto sobre a qualidade do produto.

Os administradores do sistema poderão utilizar os resultados para monitorar aspectos relacionados à estabilidade operacional, desempenho e comportamento do software em uso, identificando possíveis gargalos ou situações que possam comprometer a disponibilidade e o funcionamento adequado da aplicação.

No âmbito gerencial, a coordenação do projeto utilizará as evidências produzidas pela avaliação para apoiar a tomada de decisões sobre a evolução do sistema, definindo prioridades de manutenção, correção e implementação de novas funcionalidades. Os resultados também servirão como insumo para o planejamento de melhorias contínuas e para a alocação mais eficiente de recursos da equipe.

Embora não participem diretamente do processo de avaliação, os usuários finais serão os principais beneficiados pelos resultados obtidos. As melhorias implementadas a partir das evidências coletadas tendem a proporcionar uma experiência de uso mais intuitiva, eficiente e confiável, contribuindo para maior satisfação dos usuários e melhor atendimento às necessidades da comunidade acadêmica da Universidade de Brasília.

Assim, a avaliação não tem apenas o propósito de medir a qualidade do software, mas também de fornecer informações relevantes para apoiar ações de melhoria contínua, reduzir riscos, aumentar a satisfação dos usuários e garantir que o sistema evolua de acordo com os objetivos do projeto e as expectativas de seus stakeholders.


O cenário de aplicação da avaliação envolve o uso real do sistema web por estudantes em atividades cotidianas, considerando:

- Navegação em diferentes dispositivos;
- Execução simultânea de acessos;
- Uso contínuo das funcionalidades principais;
- Necessidade de respostas rápidas e interface intuitiva. Dessa forma, os resultados da avaliação serão usados diretamente para orientar decisões técnicas e gerenciais sobre a evolução do sistema, garantindo maior qualidade de uso e desempenho.

## Requisitante

O requisitante da avaliação é a equipe responsável pelo projeto **No Fluxo UnB**, composta pelos integrantes envolvidos nas atividades de desenvolvimento, manutenção, testes e garantia da qualidade do sistema. Como principal interessada na evolução e no desempenho do software, a equipe busca obter evidências objetivas sobre o nível de qualidade alcançado pelo produto, identificando seus pontos fortes, limitações e oportunidades de melhoria.

A avaliação é solicitada com o propósito de verificar se o sistema atende aos critérios mínimos de qualidade previamente estabelecidos para as características de **usabilidade** e **eficiência de desempenho**, consideradas essenciais para o contexto de utilização da aplicação. A usabilidade é analisada para verificar se os usuários conseguem realizar suas tarefas de forma intuitiva, eficiente e satisfatória, enquanto a eficiência é avaliada para determinar se o sistema apresenta tempos de resposta adequados e faz uso apropriado dos recursos computacionais disponíveis.

Os resultados obtidos serão utilizados como suporte à tomada de decisão da equipe, orientando ações de correção, melhoria e priorização de requisitos. Além disso, a avaliação permitirá identificar riscos relacionados à experiência do usuário e ao desempenho do sistema, fornecendo subsídios para futuras evoluções do software e contribuindo para aumentar a confiabilidade e a qualidade geral do produto entregue à comunidade acadêmica da Universidade de Brasília.

## Stakeholder

*Tabela 1: Tabela dos Stakeholders*
| Stakeholder                  | Papel no Projeto                         | Necessidades/Expectativas                              | Influência na Avaliação                                                     |
|-----------------------------|------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------------------------|
| Desenvolvedores             | Implementação e manutenção do sistema    | Identificar falhas técnicas e oportunidades de melhoria | Definem correções e evoluções a partir dos resultados                        |
| Equipe de Qualidade         | Planejamento e execução da avaliação     | Obter métricas confiáveis sobre qualidade              | Define critérios, métricas e procedimentos de avaliação                      |
| Usuários finais (estudantes)| Utilização direta da plataforma          | Facilidade de uso, rapidez e estabilidade              | Influenciam critérios de usabilidade e experiência                           |
| Administradores/Operadores  | Monitoramento e suporte do sistema       | Estabilidade operacional e baixo índice de falhas      | Influenciam requisitos de desempenho e disponibilidade                       |
| Universidade de Brasília (UnB)| Contexto institucional do sistema       | Qualidade do serviço oferecido aos estudantes          | Influencia expectativas gerais de qualidade                                   |
| Equipe de Infraestrutura    | Hospedagem e suporte técnico             | Uso eficiente de recursos computacionais               | Influencia critérios de eficiência e desempenho                               |

## Relação dos Stakeholders com a Avaliação

- As partes interessadas influenciam diretamente a definição do escopo e dos critérios da avaliação:
- Os usuários finais influenciam os critérios de usabilidade, acessibilidade e facilidade de aprendizado;
- Os desenvolvedores utilizam os resultados para priorizar correções e melhorias técnicas;
- A equipe de qualidade define métricas e interpreta os resultados obtidos;
- Os operadores e administradores contribuem para os critérios relacionados à estabilidade e desempenho;
- A instituição vinculada ao projeto influencia os padrões esperados de qualidade e confiabilidade.

O No Fluxo UNB nasceu de uma necessidade real: estudantes da UnB têm dificuldade em entender o próprio curso. Pré-requisitos confusos, equivalências mal explicadas e a dificuldade em montar uma grade que faça sentido são problemas do dia a dia. O sistema veio justamente para resolver isso — e é por isso que a qualidade do que ele entrega importa tanto.

Esta avaliação tem como foco duas dimensões que afetam diretamente a experiência de quem usa o sistema: a **Eficiência de Desempenho** e a **Confiabilidade**. Em outras palavras, queremos entender se o sistema é rápido o suficiente para não frustrar o estudante e se ele é confiável o bastante para ser usado nos momentos em que mais importa — especialmente no período de matrículas, quando muita gente acessa ao mesmo tempo e qualquer instabilidade pode ter consequências reais.

Para guiar a avaliação, partimos de três perguntas principais:

- O sistema responde em tempo hábil, tanto no uso cotidiano quanto nos picos de acesso?
- A plataforma continua funcionando mesmo quando algo externo — como o SIGAA ou a integração com a IA — apresenta instabilidade?
- Se algo der errado durante o uso, o sistema se recupera sem perda de dados ou progresso do estudante?

## Impacto da Avaliação sobre os Stakeholders

A avaliação da qualidade do sistema **No Fluxo UnB** afeta diretamente diferentes grupos envolvidos com o projeto, uma vez que seus resultados fornecem informações relevantes para decisões técnicas, operacionais e estratégicas. Como o sistema tem como objetivo auxiliar estudantes na compreensão de seus cursos, pré-requisitos, equivalências e planejamento acadêmico, garantir níveis adequados de **Eficiência de Desempenho** e **Confiabilidade** é fundamental para todos os stakeholders.

Os **desenvolvedores** são diretamente beneficiados pelos resultados da avaliação, pois as métricas coletadas permitem identificar gargalos de desempenho, falhas de integração, problemas de estabilidade e oportunidades de melhoria na arquitetura do sistema. Com base nessas evidências, a equipe pode priorizar correções, refatorações e evoluções que aumentem a qualidade do produto.

A **equipe de qualidade** utiliza os resultados para verificar se os critérios de avaliação foram atendidos e para identificar áreas que necessitam de maior atenção em futuras atividades de teste. Além disso, a avaliação fornece evidências objetivas para validar os requisitos de qualidade definidos para o projeto e aprimorar continuamente os processos de garantia da qualidade.

Os **usuários finais**, representados principalmente pelos estudantes da Universidade de Brasília, são os principais beneficiários da avaliação. Caso os resultados indiquem melhorias necessárias, a equipe poderá implementar ajustes que tornem a plataforma mais rápida, estável e confiável. Isso reduz a probabilidade de interrupções durante o uso e aumenta a confiança dos estudantes nas informações fornecidas pelo sistema, especialmente em períodos críticos, como o planejamento de disciplinas e as matrículas.

Os **administradores e operadores do sistema** são impactados porque a avaliação produz informações sobre comportamento operacional, disponibilidade e estabilidade da aplicação. Esses dados permitem identificar riscos relacionados à infraestrutura, monitorar possíveis falhas recorrentes e planejar ações preventivas para garantir a continuidade do serviço.

A **equipe de infraestrutura** utiliza os resultados para compreender como o sistema consome recursos computacionais e como se comporta sob diferentes níveis de carga. As informações obtidas podem orientar decisões relacionadas à escalabilidade, configuração de servidores, otimização de recursos e preparação para períodos de maior demanda, contribuindo para melhorar a eficiência operacional da plataforma.

Por sua vez, a **Universidade de Brasília (UnB)**, enquanto instituição beneficiada pelo projeto, é impactada de forma indireta pelos resultados da avaliação. Um sistema mais eficiente e confiável contribui para a melhoria dos serviços oferecidos à comunidade acadêmica, fortalece a confiança dos estudantes nas soluções tecnológicas da instituição e reduz problemas que possam afetar atividades acadêmicas importantes.

Dessa forma, a avaliação não se limita a medir características técnicas do software. Seus resultados influenciam decisões de desenvolvimento, manutenção, operação e gestão, contribuindo para que o No Fluxo UnB evolua de maneira alinhada às necessidades dos estudantes e às expectativas dos demais stakeholders envolvidos no projeto.

### Uso Pretendido dos Resultados

Os resultados desta avaliação não são um fim em si mesmos. A ideia é que eles sirvam de base para decisões concretas, por diferentes pessoas envolvidas com o sistema:

*Tabela 2: Relação de Partes Interessadas e Resultados*
| Parte Interessada | Como vai usar os resultados |
|---|---|
| **Desenvolvedores** | Identificar onde o sistema trava, demora ou falha — especialmente no carregamento do fluxograma, no upload do histórico e na integração com o SIGAA — e priorizar o que corrigir primeiro |
| **Equipe de Qualidade** | Verificar se as métricas definidas fazem sentido na prática e ajustar os critérios de aceitação conforme o que for encontrado |
| **Administradores / Operadores** | Acompanhar o comportamento do sistema em produção e tomar decisões sobre infraestrutura e disponibilidade |
| **Coordenação do Projeto** | Ter uma visão clara do que está funcionando bem e do que precisa de atenção para planejar os próximos passos do produto |
| **Estudantes (usuários finais)** | Embora não participem diretamente da avaliação, são os maiores beneficiados: um sistema mais rápido e estável melhora diretamente sua experiência de planejamento acadêmico |

### Cenário de Aplicação

A avaliação considera situações reais de uso do sistema — não cenários ideais ou controlados artificialmente. Isso inclui:

- Momentos de alta demanda, como os dias de abertura de matrículas, quando muitos estudantes acessam a plataforma ao mesmo tempo;
- O envio do histórico acadêmico em PDF, que pode variar bastante em tamanho e complexidade dependendo do curso e do semestre do aluno;
- A visualização de fluxogramas com muitas disciplinas e longas cadeias de pré-requisitos;
- O uso do assistente Darcy AI, que depende de uma chamada a um serviço externo (Maritaca AI) e pode sofrer com latência ou indisponibilidade;
- O acesso por dispositivos variados, desde notebooks até celulares, em condições de internet que nem sempre são as melhores.

Ao final, o que se espera é que os resultados orientem melhorias reais no sistema, de forma que o No Fluxo UNB continue crescendo com qualidade e confiança por parte de quem o usa.

## Uso de IA
IA usada para revisão ortográfica, detalhamento de uso dos resultados e definição do impacto da avaliação sobre os stakeholders

## Bibliografia 

CASA DO DESENVOLVEDOR. **Stakeholders: o que são e qual sua importância em projetos**. Disponível em: <https://blog.casadodesenvolvedor.com.br/stakeholders/>. Acesso em: 04 de junho 2026.

## Histórico de versão

| Versão | Data | Descrição | Autor |
|---|---|---|---|
| 1.0 | 11/05/26 | Criação do documento  | Julia Gabriela |
| 1.1 | 12/05/26 | Criação do pages      | Camila Careli  |
| 1.2 | 12/05/26 | Revisão do conteúdo   | Camila Careli  |
| 1.3 | 04/06/26 | Complementando contexto  | Julia Gabriela |
| 1.4 | 07/06/26 | Corrigindo formatação | Julia Gabriela |
