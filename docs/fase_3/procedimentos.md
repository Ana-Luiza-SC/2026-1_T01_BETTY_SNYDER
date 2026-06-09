## 1. Procedimentos de Avaliação

Os procedimentos de avaliação descrevem a forma como os dados serão coletados para cada métrica definida na Fase 2. Cada procedimento está associado a uma ou mais métricas, garantindo rastreabilidade entre os objetivos GQM, a massa de dados e os resultados esperados.

### 1.1 Procedimento P1 — Teste de Reconhecimento da Adequação

**Métricas relacionadas:** M1.1 e M1.2  
**Massa de dados utilizada:** MD1 e MD6  
**Objetivo:** verificar se a tela inicial comunica adequadamente o propósito da plataforma e suas funcionalidades principais.  

**Etapas:**

1. Apresentar a tela inicial do No Fluxo UnB ao participante por 5 segundos.
2. Ocultar a tela após o tempo definido.
3. Solicitar que o participante responda:

   * Qual é o objetivo principal da plataforma?
   * Quais funcionalidades você identificou?
   * A interface parece adequada para apoiar o planejamento acadêmico?
4. Registrar as respostas no formulário de coleta.
5. Aplicar uma escala Likert de 1 a 5 para medir a clareza percebida da interface.

**Dados coletados:**

*Tabela 1*
| Dado                               | Tipo         |
| :--------------------------------- | :----------- |
| Identificação correta do propósito | Quantitativo |
| Funcionalidades reconhecidas       | Quantitativo |
| Nota de clareza percebida          | Quantitativo |
| Comentários do participante        | Qualitativo  |

### 1.2 Procedimento P2 — Teste do Primeiro Fluxo Crítico

**Métricas relacionadas:** M1.3, M1.4 e M1.5  
**Massa de dados utilizada:** MD1, MD2, MD5 e MD6  
**Objetivo:** avaliar a capacidade de aprendizado do usuário no primeiro contato com a plataforma.  

**Etapas:**

1. Entregar ao participante um roteiro com a tarefa: acessar a plataforma, importar um histórico escolar em PDF e visualizar o fluxograma gerado.
2. Iniciar a cronometragem quando o participante começar a tarefa.
3. Observar a execução utilizando a técnica Think Aloud.
4. Registrar erros, dúvidas, hesitações e necessidade de ajuda externa.
5. Após a visualização do fluxograma, solicitar que o participante explique o significado de cores, legendas ou elementos visuais.
6. Solicitar uma primeira consulta ao Darcy AI.
7. Solicitar uma segunda consulta sem orientação do avaliador.
8. Encerrar a cronometragem e registrar os resultados.

**Dados coletados:**

*Tabela 2*
| Dado                                             | Tipo                     |
| :----------------------------------------------- | :----------------------- |
| Tempo total para concluir o fluxo                | Quantitativo             |
| Sucesso ou falha na tarefa                       | Quantitativo             |
| Número de dúvidas ou hesitações                  | Quantitativo             |
| Compreensão das legendas do grafo                | Quantitativo/Qualitativo |
| Capacidade de formular nova consulta ao Darcy AI | Quantitativo             |
| Observações do Think Aloud                       | Qualitativo              |

### 1.3 Procedimento P3 — Teste de Proteção contra Erros

**Métricas relacionadas:** M1.6, M1.7 e M1.8  
**Massa de dados utilizada:** MD3 e MD4  
**Objetivo:** verificar se o sistema bloqueia entradas inválidas e comunica adequadamente os erros ao usuário.  

**Etapas:**

1. Tentar realizar upload de arquivos com extensões inválidas.
2. Registrar se o sistema bloqueia o envio.
3. Tentar realizar upload de PDFs corrompidos ou fora do padrão SIGAA.
4. Registrar se o sistema identifica o problema antes ou durante o processamento.
5. Observar a mensagem de erro exibida.
6. Solicitar que o participante explique, com suas próprias palavras, o que deve ser feito para corrigir o problema.
7. Registrar se o participante conseguiu compreender a mensagem sem ajuda externa.

**Dados coletados:**

*Tabela 3*
| Dado                                      | Tipo                     |
| :---------------------------------------- | :----------------------- |
| Arquivo bloqueado corretamente            | Quantitativo             |
| PDF corrompido identificado               | Quantitativo             |
| Mensagem de erro exibida                  | Qualitativo              |
| Usuário compreendeu a correção necessária | Quantitativo/Qualitativo |

### 1.4 Procedimento P4 — Auditoria de Acessibilidade

**Métricas relacionadas:** M1.9, M1.10 e M1.11    
**Massa de dados utilizada:** MD6   
**Objetivo:** avaliar a conformidade mínima da interface com critérios de acessibilidade baseados na WCAG 2.1.  

**Etapas:**

1. Executar auditoria automatizada com Lighthouse, Axe DevTools ou WAVE.
2. Verificar contraste visual dos elementos críticos, como botões, campos de entrada, textos, alertas e nós do grafo.
3. Testar a navegação completa por teclado usando TAB, SHIFT+TAB, ENTER e ESC.
4. Verificar se os componentes interativos possuem atributos semânticos adequados, como `aria-label`, `role`, textos alternativos e hierarquia de cabeçalhos.
5. Registrar inconformidades encontradas e evidências por captura de tela ou relatório da ferramenta.

**Dados coletados:**

*Tabela 4*
| Dado                                  | Tipo                     |
| :------------------------------------ | :----------------------- |
| Elementos aprovados em contraste      | Quantitativo             |
| Elementos reprovados em contraste     | Quantitativo             |
| Funcionalidades operáveis via teclado | Quantitativo             |
| Barreiras de navegação encontradas    | Qualitativo              |
| Presença de atributos semânticos      | Quantitativo/Qualitativo |

### 1.5 Procedimento P5 — Medição de Tempo de Resposta do Fluxograma

**Métricas relacionadas:** M2.1  
**Massa de dados utilizada:** MD2  
**Objetivo:** medir o tempo decorrido entre o upload do histórico escolar e a renderização completa do grafo do fluxograma.  

**Etapas:**

1. Selecionar um histórico escolar válido.
2. Iniciar a cronometragem no momento do envio do arquivo.
3. Aguardar o carregamento completo do fluxograma.
4. Encerrar a cronometragem quando o grafo estiver visível e interativo.
5. Repetir o procedimento com históricos pequenos, médios e grandes.
6. Registrar os tempos obtidos.

**Dados coletados:**

*Tabela 5*
| Dado                              | Tipo         |
| :-------------------------------- | :----------- |
| Tempo de upload e processamento   | Quantitativo |
| Tempo até renderização completa   | Quantitativo |
| Tipo de histórico utilizado       | Categórico   |
| Ocorrência de falha ou travamento | Qualitativo  |

### 1.6 Procedimento P6 — Medição de Tempo de Resposta do Darcy AI

**Métricas relacionadas:** M2.2 e M2.3  
**Massa de dados utilizada:** MD5  
**Objetivo:** medir o tempo médio de resposta do Assistente Darcy AI e observar variações relacionadas à latência da API externa.  

**Etapas:**

1. Selecionar uma consulta padronizada.
2. Enviar a pergunta ao Darcy AI.
3. Iniciar a cronometragem no momento do envio.
4. Encerrar a cronometragem quando a resposta completa for exibida.
5. Registrar o tempo obtido.
6. Repetir a coleta em diferentes horários, preferencialmente manhã, tarde e noite.
7. Registrar falhas, lentidão perceptível ou ausência de resposta.
8. Quando possível, utilizar a aba Network do DevTools para observar o tempo das requisições associadas.

**Dados coletados:**

*Tabela 6*
| Dado                           | Tipo         |
| :----------------------------- | :----------- |
| Tempo de resposta por consulta | Quantitativo |
| Média dos tempos de resposta   | Quantitativo |
| Desvio padrão dos tempos       | Quantitativo |
| Horário da execução            | Categórico   |
| Falhas ou timeouts             | Qualitativo  |

### 1.7 Procedimento P7 — Teste de Concorrência Simulada

**Métricas relacionadas:** M2.4 e M2.6  
**Massa de dados utilizada:** MD2  
**Objetivo:** avaliar a degradação de desempenho e a taxa de sucesso do processamento em cenários de uso simultâneo.  

**Etapas:**

1. Preparar históricos escolares válidos de diferentes complexidades.
2. Executar uploads em sessões paralelas ou em janelas/navegadores distintos.
3. Simular cenários com 1, 3, 5 e 10 execuções próximas ou simultâneas.
4. Registrar o tempo de resposta de cada execução.
5. Registrar falhas, travamentos, timeouts ou inconsistências na renderização.
6. Comparar os tempos obtidos com o cenário de acesso isolado.

**Dados coletados:**

*Tabela 7*
| Dado                             | Tipo         |
| :------------------------------- | :----------- |
| Número de execuções simultâneas  | Quantitativo |
| Tempo médio por cenário          | Quantitativo |
| Tempo máximo observado           | Quantitativo |
| Taxa de sucesso no processamento | Quantitativo |
| Falhas observadas                | Qualitativo  |

### 1.8 Procedimento P8 — Inspeção de Sinalizações Visuais de Progresso

**Métricas relacionadas:** M2.5  
**Massa de dados utilizada:** MD6  
**Objetivo:** verificar se a interface apresenta indicadores visuais durante operações demoradas.  

**Etapas:**

1. Executar operações que demandem processamento, como upload de histórico, geração do fluxograma e consulta ao Darcy AI.
2. Observar se há sinalização visual durante a espera, como spinner, barra de progresso, mensagem de carregamento ou estado desabilitado de botão.
3. Registrar a presença ou ausência de feedback visual.
4. Avaliar se o feedback é perceptível e compreensível para o usuário.
5. Associar a ocorrência de sinalização visual ao tempo de execução observado.

**Dados coletados:**

*Tabela 8*
| Dado                                  | Tipo         |
| :------------------------------------ | :----------- |
| Operação avaliada                     | Categórico   |
| Presença de indicador de carregamento | Quantitativo |
| Tipo de sinalização exibida           | Qualitativo  |
| Tempo da operação                     | Quantitativo |
| Clareza da sinalização                | Qualitativo  |

### 1.9 Matriz de Rastreabilidade entre Métricas, Massa de Dados e Procedimentos

*Tabela 9*
| Métrica | Massa de Dados | Procedimento |
| :-----: | :------------- | :----------- |
|   M1.1  | MD1, MD6       | P1           |
|   M1.2  | MD1, MD6       | P1           |
|   M1.3  | MD1, MD2       | P2           |
|   M1.4  | MD1, MD6       | P2           |
|   M1.5  | MD1, MD5       | P2           |
|   M1.6  | MD3            | P3           |
|   M1.7  | MD4            | P3           |
|   M1.8  | MD1, MD4       | P3           |
|   M1.9  | MD6            | P4           |
|  M1.10  | MD6            | P4           |
|  M1.11  | MD6            | P4           |
|   M2.1  | MD2            | P5           |
|   M2.2  | MD5            | P6           |
|   M2.3  | MD5            | P6           |
|   M2.4  | MD2            | P7           |
|   M2.5  | MD6            | P8           |
|   M2.6  | MD2            | P7           |

## Uso de IA

Declaro que nesse documento fiz uso de IA para colocar no formato .md.

## Referências

<a id="ref02"></a> RAMOS, Cristiane Soares. **Processo de Avaliação de Produto de Software**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025a. Material de aula da disciplina FGA0278 — Qualidade de Software 1.

<a id="ref03"></a> RAMOS, Cristiane Soares. **Medição baseada em objetivos — Goal-Question-Metric (GQM)**. Brasília: Universidade de Brasília, Faculdade do Gama, 2025b. Material de aula da disciplina FGA0278 — Qualidade de Software 1. Baseado no material da Profa. Dra. Káthia Marçal Oliveira. Disponível em: [slide_gqm.pdf](../assets/referencia/slide_gqm.pdf).

<a id="ref05"></a> NO FLUXO UNB. **Plataforma de acompanhamento e planejamento de fluxo acadêmico**. Versão 1.0. Brasília: Crianex, 2026. Disponível em: [https://no-fluxo.crianex.com/](https://no-fluxo.crianex.com/). Acesso em: 9 jun. 2026.


## Histórico de Versão

| Versão | Data | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| 1.0 | 09/06/26 | Criação do documento de Procedimentos de Avaliação (Fase 3) | Julia Gabriela |
