# Modelo Preditivo de Overall de Jogadores do FIFA

Este projeto implementa um modelo de regressão linear para prever o **Overall** de jogadores do FIFA com base em dados extraídos de um dataset disponível no Kaggle. 

## 🔍 Objetivo
O objetivo é treinar um modelo preditivo capaz de estimar o **Overall** de um jogador a partir de atributos como velocidade, finalização, dribles, entre outros.

## 📂 Estrutura do Projeto
- **`Modelo Regressão Linear.ipynb`**: Notebook com todo o processo de modelagem preditiva, incluindo:
  - Análise exploratória de dados.
  - Tratamento de dados.
  - Criação do modelo de regressão linear.
  - Avaliação e validação do modelo.
- **`Separacao_dataset.ipynb`**: Notebook dedicado ao particionamento do dataset em conjuntos de treino e teste, além de possíveis ajustes nos dados.

## 🗂️ Dataset
O dataset foi obtido do [Kaggle](https://www.kaggle.com/) e contém informações detalhadas sobre jogadores do FIFA, incluindo atributos técnicos e físicos.

### Exemplo de Colunas no Dataset:
- `Name`: Nome do jogador.
- `Age`: Idade.
- `Potential`: Potencial do jogador.
- `Overall`: Avaliação geral do jogador (variável alvo).
- `Attributes`: Atributos técnicos e físicos, como velocidade, finalização, etc.

## 🧪 Resultados
O modelo foi avaliado usando métricas de regressão como:
- **R² Score**
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**

Os resultados indicam que o modelo é eficiente para prever o **Overall**, dentro das limitações do dataset.
