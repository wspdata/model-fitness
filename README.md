# Model Fitness — Previsão de Rotatividade e Segmentação de Clientes

## Descrição do Projeto
Projeto de análise de dados aplicado à rede de academias **Model Fitness**. O objetivo principal foi desenvolver uma estratégia de retenção de clientes baseada em dados, através da predição de rotatividade (churn) e da segmentação dos usuários em grupos com perfis distintos de comportamento e engajamento.

---

## Metodologia
1. **Pré-processamento dos dados**
   - Carregamento e inspeção do dataset, verificação de tipos e estrutura geral das variáveis.
2. **Análise Exploratória de Dados (EDA)**
   - Estatísticas descritivas, comparação de médias entre grupos (churn vs. não churn), análise de distribuições para variáveis numéricas e categóricas, e matriz de correlação entre as variáveis.
3. **Modelagem preditiva (Classificação Binária)**
   - Treinamento e avaliação de dois modelos de classificação — Regressão Logística e Floresta Aleatória — para prever a probabilidade de churn no mês seguinte.
4. **Clusterização**
   - Padronização dos dados, construção de dendrograma com linkage hierárquico (método Ward) e segmentação dos clientes em 5 grupos via K-Means.
5. **Interpretação e recomendações**
   - Análise do perfil de cada cluster, identificação dos grupos com maior risco de saída e sugestões acionáveis de retenção.

---

## Principais Insights

**Fatores que mais influenciam a rotatividade:**
- Clientes que **moram ou trabalham longe da academia** apresentam taxa de rotatividade significativamente maior — a proximidade geográfica está associada a maior retenção.
- O fator social — como entrar via **cupom de indicação de amigo** ou **treinar em grupo** — reduz as chances de cancelamento.
- Usuários de **faixa etária mais jovem** (~24 a 30 anos) apresentam maior risco de saída.
- **Clientes mais frequentes** têm bem mais fidelidade do que os de baixa frequência.
- **Contratos mais longos e com mais tempo restante** tendem a reter melhor os usuários.
- Quanto mais tempo o cliente permanece na academia, menor a chance de sair — **clientes antigos tendem a ser mais leais**.

---

## Modelos de Classificação

Ambos os modelos treinados apresentaram acurácia de **92%** nos dados de validação. A **Regressão Logística teve leve vantagem**, com precisão de 0.86 e sensibilidade de 0.83, além de ser mais interpretável para suporte à decisão de negócio.

---

## Perfil dos Clusters

- **Cluster 0 — Clientes Altamente Engajados (Churn: 3%)**
  Contratos longos, alta frequência de treinos e gastos elevados — os clientes mais fiéis da base.
  *Ações sugeridas:* Programas VIP ou de fidelidade, descontos por indicação, coleta frequente de feedback.

- **Cluster 1 — Clientes Neutros (Churn: 27%)**
  Perfil intermediário em quase todas as variáveis — nem perdido, nem plenamente engajado.
  *Ações sugeridas:* Benefícios por frequência, check-ins mensais com instrutores, relatórios de progresso personalizados.

- **Cluster 2 — Clientes Distantes e Inativos (Churn: 44%)**
  Sem proximidade com a academia e baixa frequência — indicam afastamento físico e comportamental.
  *Ações sugeridas:* Campanhas de reativação, comunicação segmentada com ofertas personalizadas, incentivos para retomada de frequência.

- **Cluster 3 — Novos Clientes com Baixo Engajamento (Churn: 51%)**
  Recém-chegados com pouca frequência e baixo engajamento — maior risco de saída precoce.
  *Ações sugeridas:* Sessões de boas-vindas obrigatórias nas primeiras semanas, mensagens automatizadas de motivação, descontos progressivos para contratos mais longos.

- **Cluster 4 — Clientes Ativos e Satisfeitos (Churn: 7%)**
  Clientes engajados e com boa frequência, mesmo com contratos mais curtos.
  *Ações sugeridas:* Programas VIP, acesso exclusivo a eventos, descontos por indicação de novos membros.

---

## 📂 Conteúdo do Repositório

- **Notebook (.ipynb):** análise completa, incluindo EDA, modelagem preditiva, clusterização e conclusões
- **README (.md):** este arquivo

---

## Tecnologias e Bibliotecas

- Linguagem: **Python**
- Bibliotecas: **pandas**, **numpy**, **matplotlib**, **seaborn**, **scikit-learn** (LogisticRegression, RandomForestClassifier, KMeans, StandardScaler), **scipy** (dendrograma hierárquico)
- Notebook: **Jupyter Notebook**

---

## Contato

Willian De Souza Pereira — ws13292@gmail.com

LinkedIn: https://linkedin.com/in/willian-de-souza-pereira-b69109202

## Licença

Este repositório está disponível para estudo e demonstração. Sinta-se à vontade para clonar, adaptar e abrir *issues* com dúvidas ou sugestões.
