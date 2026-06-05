Este trabalho foi desenvolvido no âmbito da disciplina de Qualidade de Software, com o objetivo de executar o processo de avaliação de um produto de software, aplicando metodologias e normas reconhecidas internacionalmente (Série SQuaRE - ISO/IEC 25000). A avaliação foca nas características de Usabilidade e Eficiência de Desempenho, sendo requisitada pela professora da disciplina e conduzida pela equipe do projeto. 

## Sobre o aplicativo

O [No Fluxo UNB](https://no-fluxo.crianex.com/) é um sistema web desenvolvido  por estudantes da Faculdade de Ciência e Tecnologia(FCTE), no âmbito da disciplina de Metodologia e Desenvolvimento de Software, visando auxiliar estudantes da Universidade de Brasília no planejamento acadêmico do curso. O software oferece um fluxograma interativo e personalizado, permitindo que os alunos organizem melhor sua trajetória universitária.

O principal problema que o sistema busca resolver é a dificuldade dos estudantes em entender o fluxo das disciplinas e identificar pré-requisitos e equivalências, logo se faz muito necessário seu aperfeiçoamento devido à sua importância.

## Domínio da aplicação

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

| Parte                   | Uso dos Resultados                                                     |
|------------------------|------------------------------------------------------------------------|
| Desenvolvedores        | Corrigir problemas de interface, desempenho e fluxo de navegação      |
| Equipe de qualidade    | Priorizar testes e validar requisitos de qualidade                    |
| Administradores do sistema | Monitorar estabilidade e comportamento operacional               |
| Coordenação do projeto | Apoiar decisões sobre evolução e priorização de melhorias            |
| Usuários finais        | Beneficiados indiretamente pelas melhorias implementadas             |

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

## Uso de IA
IA usada para revisão ortográfica e detalhamento de uso dos resultados

## Histórico de versão

| Versão | Data | Descrição | Autor |
|---|---|---|---|
| 1.0 | 11/05/26 | Criação do documento  | Julia Gabriela |
| 1.1 | 12/05/26 | Criação do pages      | Camila Careli  |
| 1.2 | 12/05/26 | Revisão do conteúdo   | Camila Careli  |
| 1.3 | 04/06/26 | Complementando contexto  | Julia Gabriela |
