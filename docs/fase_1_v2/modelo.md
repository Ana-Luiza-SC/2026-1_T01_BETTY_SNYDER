## Representação Gráfica do Modelo de Qualidade

O diagrama abaixo mostra como o modelo foi estruturado:

![Diagrama de Qualidade](../assets/fase1/DiagramaQualidadeDeProduto.png)

> **Legenda:**

> - **Roxo** — Usabilidade e suas subcaracterísticas (em escopo);

> - **Azul** — Eficiência de Desempenho e suas subcaracterísticas (em escopo);

> - **Cinza tracejado** — Características excluídas do escopo desta avaliação;

---

## A relação entre as duas características

Essas duas características não são independentes — elas se influenciam. Um sistema que responde dentro dos tempos esperados tende a ser mais utilizável, pois reduz a carga cognitiva do usuário durante a interação. E um sistema com boa usabilidade permite que o usuário conclua as tarefas sem erros, o que gera menos reprocessamentos e, consequentemente, menos pressão sobre o desempenho.

Na prática, analisar as duas características em conjunto contribui para entender não apenas *o que* está acontecendo, mas *por quê* — se uma dificuldade de uso tem origem em um problema de interface ou em uma limitação no tempo de resposta, por exemplo.

---

## O que ficou fora do escopo

Nem tudo do modelo ISO/IEC 25010 foi incluído. As escolhas foram intencionais:

- **Confiabilidade** e **Segurança** são características importantes para este software por conta da privacidade do usuário, mas a **Usabilidade** e **Eficiência** se destacaram como mais importantes;
- **Manutenibilidade** e **Portabilidade** não são preocupações centrais para um sistema web de acesso público nesta fase;
- Dentro de **Eficiência de Desempenho**, a subcaracterística **Capacidade** recebeu atenção por refletir a diversidade de cursos e históricos que o sistema precisa suportar;
- Dentro de **Usabilidade**, a subcaracterística **Acessibilidade** foi incluída por ser relevante para um público universitário com características variadas.

---

## Referências

- Documento elaborado com base na norma ISO/IEC 25010:2011 e nas diretrizes da disciplina FGA315 — Qualidade de Software.
- Avaliação referente ao software [No Fluxo UNB](https://no-fluxo.crianex.com/)

---

## Declaração do uso de IA

Eu, [André João Cordeiro Gomes](https://github.com/AJCGassassin), declaro que utilizei a inteligência artificial GPT para refazer o diagrama, deixando ele mais fácil de se ler.

---



## Histórico de versão

| Versão | Data | Descrição | Autor |
|---|---|---|---|
| 1.0 | 12/05/26 | Criação da página de Modelo | André João |
| 1.1 | 13/05/26 | Correção das características | Ígor Veras |
| 1.2 | 04/06/26 | Correção do diagrama e ajustes | André João |
| 1.2.1 | 06/06/2026| Ajustes finais| André João |
