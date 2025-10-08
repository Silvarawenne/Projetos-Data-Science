Projeto de Regressão: Previsão de Preços de Imóveis com Machine Learning
Este repositório contém um projeto completo de ciência de dados focado em prever os preços de venda de imóveis, utilizando o famoso dataset "Ames Housing" do Kaggle. O objetivo é aplicar um fluxo de trabalho de ponta a ponta, desde a análise exploratória e preparação dos dados até o treinamento e avaliação de um modelo de regressão.

🎯 Objetivo
Construir um modelo de Machine Learning capaz de prever o SalePrice (Preço de Venda) de um imóvel com base em suas características físicas, localização e qualidade.

📊 Dataset
O conjunto de dados utilizado é o "House Prices - Advanced Regression Techniques" do Kaggle. Ele contém 1460 registros na base de treino e 81 colunas que descrevem quase todos os aspectos de imóveis residenciais em Ames, Iowa.

Fonte: Kaggle Competition Page

⚙️ Metodologia
O projeto foi dividido nas seguintes etapas:

1. Análise Exploratória de Dados (EDA)
Análise da Variável Alvo: Investigamos a distribuição do SalePrice e identificamos uma forte assimetria à direita.

Transformação de Dados: Aplicamos uma transformação logarítmica (np.log1p) na variável alvo para normalizar sua distribuição, o que melhora a performance de muitos modelos de regressão.

Matriz de Correlação: Calculamos a correlação entre todas as variáveis numéricas e o SalePrice, visualizando os resultados em um heatmap para identificar as "pistas" mais fortes.

Principais Descobertas: As características com maior correlação positiva com o preço foram OverallQual (Qualidade Geral) e GrLivArea (Área de Estar).

Visualização das Features: Criamos gráficos de boxplot e scatterplot para confirmar visualmente a forte relação entre a qualidade/área e o preço.

2. Preparação e Modelagem
Seleção de Features: Selecionamos um subconjunto das 7 features numéricas mais correlacionadas para a criação de um primeiro modelo base.

Divisão dos Dados: Os dados foram divididos em 80% para treino e 20% para teste, utilizando train_test_split.

Escolha do Modelo: Optamos por um modelo robusto e de alta performance, o RandomForestRegressor.

3. Avaliação
O modelo treinado foi avaliado no conjunto de teste (dados nunca vistos antes) utilizando a métrica de Erro Médio Absoluto (MAE).

📈 Resultados
O modelo alcançou um Erro Médio Absoluto (MAE) de aproximadamente $19,534.81.

Isso significa que, na média, as previsões de preço do modelo erraram em cerca de 19.5 mil dólares para mais ou para menos em relação ao preço real, um resultado excelente para um modelo inicial com features selecionadas.

🛠️ Tecnologias Utilizadas
Linguagem: Python 3

Bibliotecas Principais:

Pandas para manipulação e análise de dados.

NumPy para operações numéricas e a transformação de log.

Matplotlib & Seaborn para visualização de dados.

Scikit-learn para a divisão dos dados e o modelo de Machine Learning (RandomForestRegressor).

Ambiente: O projeto foi desenvolvido no Google Colab
