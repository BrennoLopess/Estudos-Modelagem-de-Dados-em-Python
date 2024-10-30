# Análise e Modelagem de Dados em Python

Este notebook documenta cada passo do processo de modelagem de dados, dividido em 33 células. Cada célula está descrita abaixo para facilitar o entendimento e a navegação.

---

## Índice das Células

| Célula | Descrição |
|--------|-----------|
| 1      | # Engenharia de Atributos\n\nCriação de novas variáveis importantes para Análise |
| 2      | Código: #criando variavel de categoria de nivel de pagamento de acordo com a quanti... |
| 3      | Código: #visualizar dataset\ndf_dados.head() |
| 4      | Código: #Copiando DataFrame\ndf_dados_2 = df_dados.copy()\ndf_dados_2.head() |
| 5      | Código: #Cria o encoder\nlb = LabelEncoder()\n\n#Aplica o encoder nas variáveis que es... |
| 6      | Código: #visualizando as 20 primeiras linhas\ndf_dados_2.head(20) |
| 7      | Código: #Listando todas colunas do DataSet\ndf_dados_2.columns.tolist() |
| 8      | Código: # Vamos filtrar e utilizar somente as colunas necessárias\ncolumns = ['FORMA... |
| 9      | Código: #Visualizando...\ndf_dados_2.head() |
| 10     | Código: #Infos...\ndf_dados_2.info() |
| 11     | Código: plt.rcParams["figure.figsize"] = [12.00, 5.00]\nplt.rcParams["figure.autolay... |
| 12     | Código: #Separar variaveis preditoras e target\nPREDITORAS = df_dados_2.iloc[:, 0:20... |
| 13     | Código: PREDITORAS.head() |
| 14     | Código: TARGET.head() |
| 15     | Código: pip install -U joblib imbalanced-learn |
| 16     | Código: # Seed para reproduzir o mesmo resultado\nseed = 100\n\n# Cria o balanceador S... |
| 17     | Código: # Visualizando o balanceamento da variável TARGET\nplt.rcParams["figure.figs... |
| 18     | Código: # Quantidade de registros antes do balanceamento\nPREDITORAS.shape |
| 19     | Código: # Quantidade de registros antes do balanceamento\nTARGET.shape |
| 20     | Código: # Quantidade de registros após do balanceamento\nPREDITORAS_RES.shape |
| 21     | Código: # Quantidade de registros após do balanceamento\nTARGET_RES.shape |
| 22     | Código: #Quantidade de registros de balanceamento final\nTARGET_RES.shape[0] |
... (continua até a célula 33)

---

## Descrição por Célula

### Célula 1
**Descrição**: Engenharia de Atributos - Criação de novas variáveis importantes para Análise.

---

### Célula 2
**Descrição**: Código: criando variável de categoria de nível de pagamento de acordo com a quantidade de parcelas.

---

### Célula 3
**Descrição**: Código: visualizar dataset - `df_dados.head()`.

---

### Célula 4
**Descrição**: Código: Copiando DataFrame - `df_dados_2 = df_dados.copy()`.

---

### Célula 5
**Descrição**: Código: Criação do encoder e aplicação nas variáveis que precisam ser codificadas.

---

### Célula 6
**Descrição**: Código: Visualização das primeiras 20 linhas - `df_dados_2.head(20)`.

---

### Célula 7
**Descrição**: Código: Listando todas as colunas do DataSet - `df_dados_2.columns.tolist()`.

---

### Célula 8
**Descrição**: Código: Filtragem para usar apenas as colunas necessárias - seleção de colunas específicas.

---

### Célula 9
**Descrição**: Código: Visualização do DataFrame filtrado - `df_dados_2.head()`.

---

### Célula 10
**Descrição**: Código: Informações gerais do DataFrame - `df_dados_2.info()`.

---

### Célula 11
**Descrição**: Código: Configuração dos parâmetros de visualização - ajuste de tamanho de figuras.

---

### Célula 12
**Descrição**: Código: Separação de variáveis preditoras e target - seleção de colunas para análise.

---

### Célula 13
**Descrição**: Código: Visualização das variáveis preditoras - `PREDITORAS.head()`.

---

### Célula 14
**Descrição**: Código: Visualização do target - `TARGET.head()`.

---

### Célula 15
**Descrição**: Código: Instalação das bibliotecas `joblib` e `imbalanced-learn`.

---

### Célula 16
**Descrição**: Código: Definição de seed e criação de balanceador para reproducibilidade de resultados.

---

### Célula 17
**Descrição**: Código: Visualização do balanceamento da variável TARGET.

---

### Célula 18
**Descrição**: Código: Quantidade de registros antes do balanceamento - `PREDITORAS.shape`.

---

### Célula 19
**Descrição**: Código: Quantidade de registros antes do balanceamento - `TARGET.shape`.

---

### Célula 20
**Descrição**: Código: Quantidade de registros após o balanceamento - `PREDITORAS_RES.shape`.

---

### Célula 21
**Descrição**: Código: Quantidade de registros após o balanceamento - `TARGET_RES.shape`.

---

### Célula 22
**Descrição**: Código: Quantidade de registros no balanceamento final - `TARGET_RES.shape[0]`.

...


