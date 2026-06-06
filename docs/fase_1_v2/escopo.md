# Escopo, Profundidade e Objetos de Avaliação

Esta seção estabelece as fronteiras operacionais e os limites práticos para a avaliação do No Fluxo UnB. Com base no cruzamento de objetivos e restrições, definimos aqui quais funcionalidades serão testadas detalhadamente, os alvos de medição e os aspectos que foram intencionalmente deixados fora desta etapa.

## Diretrizes de Recorte

A definição do escopo desta avaliação seguiu quatro critérios práticos:

1. **Foco na Dor do Estudante:** O escopo prioriza os módulos criados para mitigar a complexidade na montagem da grade horária e na compreensão do fluxo de matérias na UnB.
2. **Avaliação Centrada no Produto (Caixa-Preta):** Como o sistema está disponível em ambiente de produção, a análise se volta para a experiência de uso externa, interações de interface e tempos de resposta perceptíveis, sem realizar inspeções no código-fonte.
3. **Esforço Concentrado:** Dedicaremos a maior parte do tempo e dos testes aos componentes visuais e de processamento de maior carga cognitiva para o usuário.
4. **Transparência nas Exclusões:** Qualquer aspectodo sistema que não for testado é registrado com sua respectiva justificativa e gatilhos para análises futuras.

---

## Dentro do Escopo

### Características Avaliadas

Decidimos concentrar nossos esforços nas duas frentes que ditam o sucesso de uso da plataforma: a fluidez da interface e a agilidade nas respostas do sistema.

* **Usabilidade:** Avalia se o estudante compreende a interface de primeira, se a densidade do grafo gera confusão visual, quão fácil é aprender a usar os recursos sem ajuda externa e se o sistema evita o envio de arquivos inválidos.
* **Eficiência de Desempenho:** Examina se o tempo de processamento para ler o histórico, gerar o gráfico dinâmico ou interagir com o assistente virtual causa frustração ou sensação de travamento.

### Módulos e Objetos sob Análise

As medições e testes práticos serão aplicados diretamente sobre os seguintes componentes da plataforma:

* **Módulo Meu Fluxograma:** Análise da clareza visual das conexões topológicas entre as matérias (grafos), a divisão por semestres e o tempo de renderização do dashboard interativo.
* **Módulo de Importação (Upload/SIGAA):** Foco na velocidade de processamento do arquivo PDF do histórico escolar e na clareza das mensagens de feedback dadas ao usuário durante o envio.
* **Assistente Darcy AI:** Avaliação do tempo de resposta nas interações de chat e na percepção de fluidez do diálogo sobre a base de regras acadêmicas da UnB.
* **Busca e Filtros de Disciplinas:** Verificação da facilidade de navegação e busca na base de dados que engloba as matrizes dos 518 cursos cadastrados.

### Cenário e Dados de Teste

A avaliação acontecerá utilizando o ecossistema real da aplicação:

* **Ambiente:** Acesso direto à URL pública de produção (https://no-fluxo.crianex.com) por meio de navegadores em computadores e smartphones, validando o comportamento responsivo.
* **Massa de Dados:** Utilização das matrizes dos 518 cursos da universidade já disponíveis no banco e envio de históricos escolares reais em formato PDF (previamente anonimizados para proteger a identidade dos estudantes).
* **Dependências Externas:** As respostas do Assistente Darcy dependerão da comunicação em tempo real com os serviços externos da Maritaca AI.

---

## Fora do Escopo

Em função do tempo disponível e do foco na experiência direta do estudante, os seguintes aspectos não farão parte deste ciclo de avaliação:

* **Auditoria de Código-Fonte:** Nosso objetivo é julgar o comportamento do produto entregue ao estudante (foco no usuário), e não a arquitetura interna ou a sintaxe do desenvolvimento.
* **Segurança Avançada e Criptografia:** Embora a privacidade do histórico acadêmico seja importante, optamos por focar na usabilidade por ser a principal barreira de engajamento atual.
* **Precisão dos Dados de Terceiros:** Não temos controle técnico sobre a exatidão dos PDFs gerados pelo SIGAA ou sobre as respostas interpretativas geradas pelo modelo linguístico da Maritaca AI.
* **Testes de Carga em Larga Escala:** Simuladores de estresse artificial de rede fogem do escopo desta avaliação acadêmica, que prioriza o comportamento no uso cotidiano.

---

## Limites de Validade das Conclusões

Os relatórios e notas gerados por esta avaliação devem ser interpretados considerando os seguintes fatores de restrição:

* **Fotografia Temporal:** O desempenho da plataforma reflete o estado do servidor e a velocidade da API da Maritaca AI nas datas específicas dos testes.
* **Amostra Qualitativa:** O grupo de testes com pelo menos 3 alunos é ideal para pescar erros graves de usabilidade na interface, mas pode não cobrir fluxos e problemas muito específicos de determinados cursos da universidade.
* **Foco no Cliente (Front-End):** Como não temos acesso às métricas internas do servidor, nossos diagnósticos de tempo são baseados puramente na percepção de quem usa a tela.

---

## Linha de Base e Ciclos Futuros

Esta é a primeira avaliação formal estruturada da plataforma **No Fluxo UnB**. Os dados colhidos aqui funcionarão como uma **linha de base (*baseline*)** — um ponto de partida documentado. 

No futuro, quando a equipe realizar melhorias na interface ou otimizações no processamento de grafos, os novos testes poderão ser comparados com este documento para provar, por meio de dados, o quanto o sistema evoluiu em agilidade e facilidade de uso.

---

## Referências

<a id="ref01"></a>NO FLUXO UNB. **Plataforma de acompanhamento e planejamento de fluxo acadêmico**. Versão 1.0. Brasília: Crianex, 2026. Disponível em: [https://no-fluxo.crianex.com/](https://no-fluxo.crianex.com/). Acesso em: 5 jun. 2026.

<a id="ref02"></a>RAMOS, Cristiane Soares. **Processo de Avaliação de Produto de Software**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025. Material de aula da disciplina FGA0278 - Qualidade de Software.

---

## Declaração do uso de IA

Eu, [Daniel Nascimento](https://github.com/zDrNz), declaro que utilizei a inteligência artificial Gemini para a estruturação textual, refinamento gramatical e adaptação do estilo de escrita com base nos padrões estabelecidos pelo projeto.

---

## Histórico de versão

| Versão | Data | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| 1.0 | 05/06/26 | Escrita e estruturação do escopo, profundidade e objetos de avaliação | [Daniel Nascimento](https://github.com/zDrNz) |