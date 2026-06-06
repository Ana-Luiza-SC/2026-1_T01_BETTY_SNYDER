# Características de Qualidade Selecionadas

De acordo com o [processo de avaliação de produto de software](#ref03), a definição das características de qualidade deve partir dos objetivos da avaliação e das necessidades do [requisitante](objetivo_avaliacao.md), estabelecendo quais aspectos do produto serão analisados e qual a importância atribuída a cada um deles [[3]](#ref03).

Em suma, foram selecionadas as características **Usabilidade** e **Eficiência de Desempenho**, por serem os aspectos que exercem maior impacto na experiência dos estudantes durante a utilização do sistema.

---

## Ênfase das Características

A definição da ênfase foi realizada seguindo a escala proposta no processo de avaliação, variando de 1 (nenhum interesse) a 5 (grande interesse) [[3]](#ref03).

| Característica | Ênfase | Justificativa |
| :--- | :---: | :--- |
| **Usabilidade** | 5 | O sistema é utilizado diretamente por estudantes, exigindo uma interface intuitiva, de fácil aprendizado e compreensão. |
| **Eficiência de Desempenho** | 5 | O processamento dos históricos acadêmicos e a geração dos fluxogramas devem ocorrer de forma rápida, garantindo uma experiência satisfatória aos usuários. |
| **Funcionalidade** | 3 | Embora importante, a avaliação não possui foco na validação funcional completa do sistema nesta etapa. |
| **Confiabilidade** | 2 | Não constitui o principal objetivo da avaliação atual. |
| **Completitude** | 2 | Não constitui o principal objetivo da avaliação atual. |
| **Portabilidade** | 1 | Não faz parte do escopo definido para esta avaliação. |

<center><sub>Tabela 1 — Ênfase atribuída às características de qualidade do produto.</sub></center>

### Justificativa da Seleção

A escolha dessas características foi realizada devido à sua relação direta com o objetivo do sistema e com as necessidades dos usuários finais.

Como o No Fluxo UNB é uma ferramenta de apoio ao planejamento acadêmico, é fundamental que os estudantes consigam utilizá-la facilmente e obtenham resultados de forma rápida.

Por esse motivo, as características de Usabilidade e Eficiência de Desempenho receberam a maior prioridade dentro do escopo desta avaliação.

---

## Detalhamento das Características e Subcaracterísticas
Essas atribuições foram realizadas por meio de uma análise consultiva e técnica da equipe de avaliação, cruzando o comportamento esperado da plataforma com o perfil do usuário universitário.

- O **impacto** mensura a severidade do dano causado à experiência do estudante caso a subcaracterística falhe.
 - O **risco** indica a probabilidade de ocorrência dessa falha na prática, considerando fatores críticos de infraestrutura, como a instabilidade na comunicação com APIs externas, o volume de acessos simultâneos em períodos de matrícula e a integridade dos arquivos gerados pelo SIGAA.


### 1. Usabilidade

Refere-se à capacidade do software de permitir que seus usuários atinjam seus objetivos de maneira eficaz, eficiente e satisfatória [[1]](#ref01). No ecossistema do No Fluxo UNB, os usuários precisam compreender rapidamente a interface, realizar ações sem treinamento prévio e interpretar dados acadêmicos com facilidade.

| Subcaracterística de Usabilidade (SQuaRE) | Impacto | Risco | Justificativa |
| :--- | :--- | :--- | :--- |
| **Reconhecimento da Adequação** | Alto | Médio | Avalia se o estudante, ao acessar o sistema pela primeira vez, consegue perceber que a ferramenta serve para planejar sua grade curricular a partir do upload do histórico do SIGAA, evitando abandono precoce da página. |
| **Capacidade de Aprendizado** | Alto | Alto | Mede a facilidade com que o discente compreende de forma autônoma o fluxo operacional (fazer o upload, selecionar o curso e ler o gráfico), dado que o sistema não possui canais de suporte em tempo real ou treinamentos. |
| **Proteção contra Erros do Usuário** | Alto | Alto | Verifica se o sistema previne falhas críticas do usuário, como o envio de PDFs corrompidos/inválidos ou escolha de matrizes curriculares incompatíveis com sua habilitação real. |
| **Acessibilidade** | Alto | Médio | Avalia a adaptação da interface para garantir que discentes com diferentes capacidades visuais, motoras ou cognitivas utilizem a plataforma em igualdade de condições dentro da universidade [[3]](#ref03). |

<center><sub>Tabela 2 — Classificação das subcaracterísticas de Usabilidade.</sub></center>

### 2. Eficiência de Desempenho

Está relacionada à capacidade do sistema de apresentar níveis adequados de desempenho considerando a quantidade de recursos utilizados sob condições específicas [[1]](#ref01). Tempos elevados de resposta no ambiente web comprometem diretamente a utilidade prática da ferramenta durante o planejamento de matrícula discente [[3]](#ref03).

| Subcaracterística de Eficiência (SQuaRE) | Impacto | Risco | Justificativa |
| :--- | :--- | :--- | :--- |
| **Comportamento em Relação ao Tempo** | Alto | Alto | Examina o tempo de resposta gasto pela aplicação para processar a base de dados curriculares e renderizar o grafo visual do fluxograma. Gargalos aqui geram alta frustração em períodos de pico (como semanas de matrícula). |
| **Capacidade** | Médio | Alto | Verifica a estabilidade do sistema ao processar históricos escolares de extensões variadas e com grandes volumes de disciplinas acumuladas, sem causar estouro de memória ou travamentos na API. |

<center><sub>Tabela 3 — Classificação das subcaracterísticas de Eficiência de Desempenho.</sub></center>

---

## Referências

<a id="ref01"></a>INTERNATIONAL ORGANIZATION FOR STANDARDIZATION (ISO). **ISO/IEC 25000:2014 - Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — Guide to SQuaRE**. Geneva: ISO, 2014. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards>.

<a id="ref02"></a>NO FLUXO UNB. **Plataforma de acompanhamento e planejamento de fluxo acadêmico**. Versão 1.0. Brasília: Crianex, 2026. Disponível em: <https://no-fluxo.crianex.com/>.

<a id="ref03"></a>RAMOS, Cristiane Soares. **Processo de Avaliação de Produto de Software**. Brasília: Universidade de Brasília, Faculdade do Gama, 2026. Material de aula da disciplina FGA0278 - Qualidade de Software. Disponível em: [slide_processo_avaliacao.pdf](../assets/referencia/slide_processo_avaliacao.pdf).

## Declaração do uso de IA

Eu, [Camila Careli](https://github.com/camilascareli), declaro que utilizei o ChatGPT para colocar as informações em arquivo markdown.

## Histórico de Versão

| Versão | Data | Descrição | Autor |
|---------|------------|------------|------------|
| 1.0 | 11/05/26 | Criação do documento | Julia Gabriela |
| 1.1 | 12/05/26 | Criação do Pages | Camila Careli |
| 1.2 | 12/05/26 | Revisão do conteúdo | Camila Careli |
| 1.3 | 06/06/26 | Definição das características selecionadas, justificativas, referências e revisão do conteúdo | Camila Careli |
| 2.0 | 06/06/26 | Adição das subcaracterísticas | Camila Careli |