# Análise e Modelagem de Dados em Python

Este notebook documenta cada passo do processo de modelagem de dados, dividido em 26 células. Cada célula está descrita abaixo para facilitar o entendimento e a navegação.

---

## Índice das Células

| Célula | Descrição |
|--------|-----------|
| 27      | Importação de Bibliotecas |
| 28      | Coletando Dados |
| 29      | Formato dos dados |
| 30      | Introdução dos dados |
| 31      | Informações dos dados |
| 32      | Data dos Dados |
| 33      | Descrição dos dados |
| 34      | Valores Nulos do DataFrame |
| 35      | Valores Únicos dos dados |
| 36     | Agrupando Variável Categórica |

---

## Descrição por Célula

### Célula 27
**Descrição**: _Importando as bibliotecas e pacotes necessários para as análises_.

---

### Célula 28
**Descrição**: _Coletando os dados do arquivo csv, os dados são a respeito de uma empresa de televisão_.

---

### Célula 29
**Descrição**: _Utilizei a função .shape para ter informações de quantos registros e quantas variáveis existem no dataframe_.

---

### Célula 30
**Descrição**: _Usei a função .head() para ver as 5 primeiras linhas do dataframe_.

---

### Célula 31
**Descrição**: _Implantei a função .info() para ver qual tipo das variáveis. Foi Possível notar 7 objects, que seriam 7 do tipo 'String', além de 1 do tipo 'float' e 16 do tipo 'int' que seriam os inteiros_.

---

### Célula 32
**Descrição**: _Utilizei a função de date_time para checar a data máxima e a data mínima dos dados, onde foi checado que os dados coletados foram de 2001 até 2021_.

---

### Célula 33
**Descrição**: _Utilizei a função .describe() para ver um resumo estatístico dos números dos dados do dataframe_.

---

### Célula 34
**Descrição**: _Passo importante para análise! Utilizei uma nova função .isna() para verificar os valores missing do dataframe, ou seja os valores que constam NaN. A função sum() serve para somá-los e facilitar a visualização_.

---

### Célula 35
**Descrição**: _Utilizei a função .nunique() para verificar os valores únicos, importante para a análise para ter uma visão das variáveis categóricas e numéricas. Quando há um grande número de valores, pode significar que não seja categórico e que seja uma propriedade exclusiva de cada Variável, tornando-a Numérica_.

---

### Célula 36
**Descrição**: _Após a análise de Variáveis categóricas, foram selecionadas 5 importantes para o resto da análise. Assim, foi utilizado a função groupby(['NOME_DA_VARIÁVEL']).size() para verificar quantos existem quantos existem em cada tipo. Na primeira 'FORMA_AQUISICAO' foi possível ver 2 tipos, Site e Vendedor assim como seus respectivos valores_.

---

