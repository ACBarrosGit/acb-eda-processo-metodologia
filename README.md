# acb-eda-processo-metodologia
Metodologia estruturada de EDA: da pergunta inicial até insights acionáveis. checklist prático para análise exploratória de dados

# Exploratory Data Analisys
O Processo EDA é uma metodologia estruturada para conduzir análises exploratórias de dados de forma organizada e eficiente. O fluxo — Pergunta → KPI → Hipóteses → Sanity Check → Univariada → Bivariada → Multivariada → Priorização — serve como checklist prático que vai do alinhamento inicial até a geração de insights acionáveis, garantindo consistência, clareza e impacto na tomada de decisão


*Pergunta → KPI → Hipóteses → Sanity Check → Univariada → Bivariada → Multivariada → Priorização)*

---

## **1️⃣ Alinhamento e Escopo**

Essa é a fase em que será desenhada a coluna vertebral do estudo, onde serão definidos os KPIs de sucesso e insucesso do projeto.

- **Reunião inicial** com stakeholders.
- **Definir a pergunta central** que o EDA precisa responder.
- **Listar hipóteses** que possam explicar a pergunta.
- **Associar um KPI central** à pergunta principal.
- Para cada hipótese → **mapear variáveis/dados correspondentes**.

---

## **2️⃣ Sanity Check – KPI Central**

Com a pergunta da análise definida e, consequentemente, o KPI principal (variável dependente), torna-se necessário avaliar a qualidade do dado, a forma como está disponibilizado e se atende às necessidades da análise.

- Verificar completude, integridade e consistência dos dados do KPI.
- Conferir tipo de dado, formato, duplicatas e intervalos plausíveis.
- **Se reprovado** → acionar **Plano B** (nova coleta, uso de proxy, redefinição).

---

## **3️⃣ Análise Univariada – KPI Central**

Aqui o foco é um primeiro contato com o KPI central: compreender seu comportamento, granularidade e outras características.

- **Se numérico**: histograma, boxplot, métricas de resumo, análise temporal.
- **Se categórico**: tabela de frequência, gráfico de barras, evolução temporal.
- Objetivo: entender o comportamento isolado do KPI.

---

## **4️⃣ Sanity Check – Variáveis das Hipóteses**

Com a pergunta e as hipóteses definidas, é hora de verificar quais dados das hipóteses estão disponíveis e como se relacionam com o KPI principal. Essa etapa ajuda a refinar quais hipóteses devem ser priorizadas no início da análise.

- Aplicar os mesmos testes de integridade e consistência usados no KPI.
- **Se reprovadas** → reduzir prioridade ou descartar a hipótese.

---

## **5️⃣ Análise Univariada – Variáveis Priorizadas**

Aqui o foco é um primeiro contato com as variáveis independentes (dados das hipóteses), entendendo seus comportamentos e granularidades.

- Seguir a mesma lógica da univariada do KPI.
- Entender o comportamento isolado de cada variável antes dos cruzamentos.

---

## **6️⃣ Análise Bivariada**

Com a definição do KPI principal, os dados das hipóteses e seus comportamentos, é preciso analisar quanto cada variável impacta o KPI, visando responder à pergunta inicial do problema.

Por definição, as variáveis são classificadas em Numéricas ou Categóricas. Assim, as análises seguem:

### **a) Numérica vs Numérica**

- Correlação (Pearson, Spearman, Kendall).
- Dispersão (scatter plot) com linha de tendência.
- Evolução conjunta ao longo do tempo.
- Possível categorização para facilitar a leitura.

### **b) Numérica vs Categórica**

- Distribuição da variável numérica por categoria (boxplot, histograma).
- Teste t / ANOVA (paramétrico).
- Mann-Whitney / Kruskal-Wallis (não paramétrico).

### **c) Categórica vs Categórica**

- Tabela de contingência.
- Gráfico de barras agrupadas ou empilhadas.
- Teste de proporção ou Qui-Quadrado.

## **7️⃣ Análise Multivariada**

Essa é a etapa em que as variáveis deixam de ser analisadas de forma isolada ou em pares, e passam a ser estudadas em conjunto. O objetivo é entender como várias variáveis ao mesmo tempo se relacionam com o KPI principal, identificando padrões mais complexos que não aparecem em análises univariadas ou bivariadas.

- **Selecionar variáveis mais relevantes** com base na análise bivariada anterior.
- **Aplicar modelos explicativos** para captar relações multivariadas:
    - Regressão linear ou logística para medir impacto direto.
    - Árvores de decisão para identificar segmentações.
    - GAMs, PCA ou clusterização quando fizer sentido.
- **Validar relevância das variáveis** com métricas de importância (SHAP, LIME, Feature Importance).
- **Interpretar efeitos combinados** das variáveis sobre o KPI central.
- 
## **8️⃣ Priorização e Insights**

Com todos os testes e análises feitos, essa é a fase de organização e síntese. O foco é transformar o que foi descoberto em conhecimento acionável para o projeto, facilitando a tomada de decisão.

- **Rankear hipóteses** de acordo com a força da evidência observada.
- **Destacar variáveis mais impactantes** no KPI central.
- **Identificar gaps**: dados insuficientes, variáveis relevantes que faltam ou precisam de melhor qualidade.
- **Gerar recomendações práticas** que orientem próximos passos do projeto ou decisões estratégicas.

# Licença

- Código e exemplos → [MIT License](LICENSE)  
- Conteúdo e textos → [CC BY 4.0](LICENSE-CC-BY.md)  

Você pode usar, adaptar e compartilhar este material livremente, **desde que dê o devido crédito à autora: Carol Barros**.

