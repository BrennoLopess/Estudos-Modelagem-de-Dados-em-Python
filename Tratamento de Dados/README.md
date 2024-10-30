# Análise e Modelagem de Dados em Python

Este notebook documenta cada passo do processo de modelagem de dados, dividido em 26 células. Cada célula está descrita abaixo para facilitar o entendimento e a navegação.

---

## Índice das Células

| Célula | Descrição |
|--------|-----------|
| 27      | Montando novo DataFrame |
| 28      | Agrupando Variável |
| 29      | Mediana, Média e Moda |
| 30      | Preenchendo Valores Nulos |
| 31      | Trocando Tipo de Variável Categórica |
| 32      | Visualizando linhas do novo DataSet |
| 33      | Informações do novo DataSet |
| 34      | Tratando Outlier |
| 35      | Alterando Registros |
| 36     | Checando o Tratamento do Outlier |

---

## Descrição por Célula

### Célula 27
**Descrição**: _Monto Um novo DataFrame chamado 'df_dados' que é a cópia do antigo DataFrame 'df_original', porém coloco a variável QT_FILHOS pegando os registros que possuem apenas 2 ou menos 'filhos'. Esse novo Dataframe exclui os valores antes discrepantes da variável citada. Como são apenas 4 casos, não tem problema de excluí-los _.

---

### Célula 28
**Descrição**: _Faço um groupby da variável QT_FILHOS para checar se foram excluídos do novo Dataframe os valores absurdos de 17 ou mais filhos_.

---

### Célula 29
**Descrição**: _Calculo a Média, mediana e moda da variável QT_FILHOS pois além desses outliers já tratados a variável constava 254 valores nulos, então irei preenche-los com a mediana da variável_.

---

### Célula 30
**Descrição**: _Uso a função fillna() para preencher os valores nulos com a mediana da variável com a função median(). Após isso, na segunda linha, faço o mesmo código feito anteriormente para checar os valores nulos e ver se foi corrigido com sucesso_.

---

### Célula 31
**Descrição**: _Na variável 'DURACAO_CONTRATO' foi analisado que estava em objeto, ou seja, em formato de string. Para deixar o DataFrame apenas com valores numéricos e sem strings, irei alterar a variável para ao invés de '24 meses' ser apenas o número 24. Fiz isso com os 4 tipos e deixei em formato de inteiro_.

---

### Célula 32
**Descrição**: _Dou um head() para visualizar como ficou a variável com o novo modelo apenas com os números_.

---

### Célula 33
**Descrição**: _Utilizo a função info() novamente para checar o tipo da variável para ver se foi trocado com sucesso. É possível perceber que não consta mais como 'object' e sim como 'int64'_.

---

### Célula 34
**Descrição**: _Irei tratar a última Outlier analisada referente ao número de parcelas. A quantidade máxima de parcelas possível seria de 48, já que condiz com o número máximo de contrato oferecido pela empresa, que seria os 48 meses que acabamos de alterar. Com isso, pego as duas variáveis 'QT_PC_PAGAS' e 'QT_PC_PAGA_EM_DIA' que trazem informações sobre parcelas e dou um print para ver seu valor máximo, dado, de maneira errada, como 100_.

---

### Célula 35
**Descrição**: _Altero o valor máximo das duas variáveis para ficar de acordo com o valor máximo da DURACAO_CONTRATO que seria os 48 meses_.

---

### Célula 36
**Descrição**: _Apenas faço um print para verificar a quantidade máxima de parcelas. Consigo analisar que foi trocado com sucesso_.

---

