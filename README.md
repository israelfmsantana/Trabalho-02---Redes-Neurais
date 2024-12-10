Relatorio

Objetivo do Projeto
O objetivo deste projeto é analisar e classificar ataques de cibersegurança, utilizando tanto métodos de aprendizado de máquina tradicionais (como Random Forest) quanto redes neurais profundas (TensorFlow/Keras). O projeto busca entender os padrões dos ataques, melhorar o desempenho dos modelos e encontrar insights relevantes no dataset.


Etapas do Desenvolvimento

1. Pré-processamento e Análise Exploratória dos Dados (EDA)
Foram realizadas análises iniciais do dataset com foco no tratamento dos dados.

1.1 Leitura e Carregamento dos Dados
•	Os dados foram carregados a partir de um arquivo CSV com a coluna cybersecurity_attacks.csv.
•	Utilizamos o pandas para manipulação e inspeção das informações.

1.2 Limpeza dos Dados
•	Valores Duplicados: Foram removidos duplicatas para evitar redundância.
•	Valores Ausentes: Identificamos valores ausentes e os preenchemos com a mediana das colunas numéricas.
•	Outliers: Usamos o método de Interquartile Range (IQR) para detectar possíveis outliers em variáveis numéricas.

1.3 Visualização e Análise Exploratória
•	Distribuição das Variáveis: Usamos sns.countplot e matplotlib para verificar a distribuição das variáveis.
•	Correlação: Criamos heatmaps para analisar a correlação entre as colunas numéricas, identificando padrões relevantes entre métricas.

2. Modelagem com Aprendizado de Máquina (Random Forest)
Depois do pré-processamento, implementamos o treinamento e avaliação do modelo utilizando o RandomForestClassifier do scikit-learn.

2.1 Pré-processamento dos Dados
•	Normalização das Variáveis Numéricas: Utilizamos o StandardScaler para padronizar todas as variáveis numéricas.
•	Codificação das Variáveis Categóricas: Usamos o LabelEncoder para transformar variáveis categóricas em valores numéricos.

2.2 Treinamento e Avaliação do Modelo Random Forest
•	Dividimos o dataset em conjuntos de treino e teste (80% treino e 20% teste).
•	Usamos o RandomForestClassifier e avaliamos a performance do modelo com métricas como Acurácia e Relatório de Classificação.
•	Para otimizar o desempenho, aplicamos o RandomizedSearchCV, buscando os melhores parâmetros do modelo.

3. Detecção de Outliers e Análise Temporal
Para entender melhor os padrões dos ataques:
•	Detecção de Outliers: Usamos o método do Interquartile Range (IQR) para identificar anomalias relevantes.
•	Análise Temporal: Convertendo a coluna Timestamp em colunas adicionais (Ano, Dia da Semana, etc.) para investigar padrões sazonais e diários.

4. Criação do Modelo de Rede Neural
Para aumentar a complexidade do aprendizado e melhorar a performance da classificação:

4.1 Pré-processamento
•	Realizamos a normalização das variáveis numéricas e a codificação das variáveis categóricas.

4.2 Desenvolvimento das Redes Neurais
•	Criamos um método, que permite testar várias configurações das camadas e seus neurônios.
•	Testamos 3 topologias de rede neural, com as seguintes configurações de camadas:
o	Topologia 1: 2 camadas (128 e 64 neurônios)
o	Topologia 2: 2 camadas (256 neurônios cada)
o	Topologia 3: 3 camadas (128, 64 e 32 neurônios)
•	Treinamos o modelo em 10 épocas com um tamanho de batch de 64.


Conclusão
O projeto mostrou que é possível combinar métodos clássicos e avançados de aprendizado de máquina para criar modelos robustos na detecção e classificação de ataques de cibersegurança. Com as análises exploratórias, a detecção de outliers e a experimentação das topologias das redes neurais, foi possível entender os padrões dos ataques e otimizar os modelos para alcançar precisão e desempenho consistentes.
