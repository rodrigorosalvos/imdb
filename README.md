# Análise de Filmes IMDb
## Descrição

Este projeto analisa dados de filmes do IMDb para ajudar um estúdio a decidir qual tipo de filme produzir. Inclui análise exploratória de dados (EDA) e um modelo de machine learning para prever notas do IMDb.

## Como instalar e executar o projeto

### 1. Requisitos

- Python 3.8 ou superior
- Jupyter Notebook

### 2. Instalação

1. Baixe o projeto
   ```bash
   # Se estiver no GitHub
   git clone <link-do-repositorio>
   cd projeto-imdb
   ```

2. Instale as bibliotecas necessárias
   ```bash
   pip install -r requirements.txt
   ```

   As bibliotecas necessárias são:
   - pandas 2.2.2
   - numpy 2.0.2
   - matplotlib 3.10.0
   - seaborn 0.13.2
   - scikit-learn 1.6.1
   - xgboost 3.0.4
   - joblib 1.5.2

### 3. Executar o projeto

1. Inicie o Jupyter Notebook
   ```bash
   jupyter notebook
   ```

2. Abra o arquivo principal
   - Clique em `LH_CD_RODRIGOROSALVOS.ipynb`

3. Execute as células
   - Execute uma célula por vez (Shift + Enter)
   - Ou execute todas: Ambiente de execução → Executar tudo

## Arquivos do projeto

- `LH_CD_RODRIGOROSALVOS.ipynb` - Notebook principal com todas as análises
- `desafio_indicium_imdb.csv` - Dados dos filmes
- `modelo_xgb.pkl` - Modelo treinado
- `requirements.txt` - Lista das bibliotecas necessárias

## Relatórios das análises

### Análise Exploratória de Dados (EDA)

O notebook contém as seguintes análises:

#### 1. Distribuições das variáveis
- Histograma das notas IMDb
- Distribuição da duração dos filmes
- Distribuição do Meta Score
- Distribuição do faturamento dos filmes
- Top 10 diretores com mais filmes
- Top 10 gêneros mais frequentes

#### 2. Correlações
- Matriz de correlação entre variáveis numéricas

#### 3. Análise textual
- Nuvem de Palavras mais frequentes em Overview

### Perguntas respondidas

1. Qual filme recomendar para uma pessoa desconhecida?
   - Resposta: The Godfather

2. Fatores relacionados com alto faturamento:
   - Número de votos (popularidade)
   - Gêneros de ação e aventura
   - Duração adequada (120-180 min)

3. Insights da sinopse:
   - É possível inferir parcialmente o gênero pelas palavras
   - Cada gênero tem vocabulário característico

4. Como prever nota IMDb:
   - Modelo de regressão usando XGBoost
   - Variáveis importantes: Meta Score, número de votos, gênero, overview

### Resultados do modelo

- Tipo: Regressão (prever nota de 1 a 10)
- Algoritmo: XGBoost
- Erro médio: 0.15 pontos na escala IMDb
- Principais variáveis: Duração, número de votos, Meta Score

  
