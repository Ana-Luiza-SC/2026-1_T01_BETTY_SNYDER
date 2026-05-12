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

### Uso Pretendido dos Resultados

Os resultados desta avaliação não são um fim em si mesmos. A ideia é que eles sirvam de base para decisões concretas, por diferentes pessoas envolvidas com o sistema:

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

---

## Histórico de versão

| Versão | Data | Descrição | Autor |
|---|---|---|---|
| 1.0 | 12/05/26 | Criação da página inicial | Camila Careli |
| 1.1 | 12/05/26 | Revisão do conteúdo | Camila Careli |