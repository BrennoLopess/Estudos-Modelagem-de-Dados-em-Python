# Análise e Modelagem de Dados em Python

Este notebook documenta cada passo do processo de modelagem de dados, dividido em 29 células. Cada célula está descrita abaixo para facilitar o entendimento e a navegação.

---

## Índice das Células

| Célula | Descrição |
|--------|-----------|
| 1      | Importação de Bibliotecas |
| 2      | Coletando Dados |
| 3      | Formato dos dados |
| 4      | Introdução dos dados |
| 5      | Informações dos dados |
| 6      | Data dos Dados |
| 7      | Descrição dos dados |
| 8      | Valores Nulos do DataFrame |
| 9      | Valores Únicos dos dados |
| 10     | Agrupando Variável Categórica |
| 11     | Agrupando Variável Categórica |
| 12     | Agrupando Variável Categórica |
| 13     | Agrupando Variável Categórica |
| 14     | Agrupando Variável Categórica |
| 15     | Gráfico Status por Sexo e Forma Aquisição |
| 16     | Gráfico Status por Duração de Contrato |
| 17     | Gráfico Status por Tipo de Plano |
| 18     | Gráfico de Status dos clientes |
| 19     | Visualizando Variáveis numéricas |
| 20     | Quantidade de Variáveis numéricas |
| 21     | Boxplot para Outliers |
| 22     | Possível Outlier |
| 23     | Identificação de Outliers |
| 24     | Agrupando um Outlier |
| 25     | Indentificado um Outlier |
| 26     | Verificando quais registros tem Outlier |

---

## Descrição por Célula

### Célula 1
**Descrição**: _Importando as bibliotecas e pacotes necessários para as análises_.

---

### Célula 2
**Descrição**: _Coletando os dados do arquivo csv, os dados são a respeito de uma empresa de televisão_.

---

### Célula 3
**Descrição**: _Utilizei a função .shape para ter informações de quantos registros e quantas variáveis existem no dataframe_.

---

### Célula 4
**Descrição**: _Usei a função .head() para ver as 5 primeiras linhas do dataframe_.

---

### Célula 5
**Descrição**: _Implantei a função .info() para ver qual tipo das variáveis. Foi Possível notar 7 objects, que seriam 7 do tipo 'String', além de 1 do tipo 'float' e 16 do tipo 'int' que seriam os inteiros_.

---

### Célula 6
**Descrição**: _Utilizei a função de date_time para checar a data máxima e a data mínima dos dados, onde foi checado que os dados coletados foram de 2001 até 2021_.

---

### Célula 7
**Descrição**: _Utilizei a função .describe() para ver um resumo estatístico dos números dos dados do dataframe_.

---

### Célula 8
**Descrição**: _Passo importante para análise! Utilizei uma nova função .isna() para verificar os valores missing do dataframe, ou seja os valores que constam NaN. A função sum() serve para somá-los e facilitar a visualização_.

---

### Célula 9
**Descrição**: _Utilizei a função .nunique() para verificar os valores únicos, importante para a análise para ter uma visão das variáveis categóricas e numéricas. Quando há um grande número de valores, pode significar que não seja categórico e que seja uma propriedade exclusiva de cada Variável, tornando-a Numérica_.

---

### Célula 10
**Descrição**: _Após a análise de Variáveis categóricas, foram selecionadas 5 importantes para o resto da análise. Assim, foi utilizado a função groupby(['NOME_DA_VARIÁVEL']).size() para verificar quantos existem quantos existem em cada tipo. Na primeira 'FORMA_AQUISICAO' foi possível ver 2 tipos, Site e Vendedor assim como seus respectivos valores_.

---

### Célula 11
**Descrição**: _Usado novamente groupby para variável 'SEXO' sendo possível ver que existe 'Masculino' e 'Feminino' e seus respectivos valores_.

---

### Célula 12
**Descrição**: _groupby utilizado na variável 'DURACAO_CONTRATO'. Foi possível analisar que existem 4 tipos: 12 Meses, 24 Meses, 36 Meses e 48 Meses. Porém esses dados estão em formato de string, ou seja, objeto. Iremos mudar esse tipo mais para frente no tratamento dos dados_.

---

### Célula 13
**Descrição**: _groupby utilizado na variável 'NOME_PRODUTO', sendo possível ver 6 nomes que constam o tipo de plano que são: 
PLANO BASICO (30 CANAIS HD)
PLANO BASICO PLUS (50 CANAIS HD)
PLANO FAMILIA (100 CANAIS HD)
PLANO MEDIO A (60 CANAIS HD)
PLANO MEDIO TOP (90 CANAIS HD)
PLANO PREMIUM TOTAL_.

---

### Célula 14
**Descrição**: _Groupby utilizado na variável 'Situacao' sendo possível ver 2 tipos: Cancelado ou ativo._.

---

### Célula 15
**Descrição**: _Plotando gráficos para visualizar o SEXO e a FORMA_AQUISICAO de acordo com a SITUACAO do cliente, ou seja, vendo se está cancelado ou ativo. Gráficos ficam mais fáceis para visualização pois é possível ver se há alguma discrepância_.

---

### Célula 16
**Descrição**: _Seguindo a mesma lógica dos gráficos, agora visualizando a DURACAO_CONTRATO de acordo com a SITUACAO de cancelado ou ativo. Foi possível analisar que a maioria dos planos são de 48 meses_.

---

### Célula 17
**Descrição**: _Agora, visualizando o tipo do plano, ou seja o nome do produto de acordo com a situação do cliente, se está ativo ou cancelado. Percebe-se que o plano Básico foi o mais utilizado e o que possui os maiores números.

---

### Célula 18
**Descrição**: _Agora apenas plotando gráfico para visualizar quantos clientes estão ativos e quantos estão cancelados. Apenas a SITUACAO está sendo analisada neste gráfico. Foi possível analisar a discrepância entre os dois, sendo o ATIVO muito mais que o CANCELADO. Precisaremos balancear na etapa de tratamento de dados._.

---

### Célula 19
**Descrição**: _Aqui, saímos das variáveis categóricas e passamos a analisar as numéricas. O codigo usado foi para automatizar o processo de mostrar apenas as variáveis numéricas, ou seja, que é do tipo 'int64' ou 'float64' e reservando-as na lista 'variaveis_numéricas'_.

---

### Célula 20
**Descrição**: _Fazendo a função len() para apenas verificar o tamanho da lista, desse modo, vendo quantas variáveis numéricas existem_.

---

### Célula 21
**Descrição**: _Realizo Boxplots que seria uma das formas ´para visualizar possíveis OUTLIERS que serão corrigidos na parte dos tratamentos dos dados. Por esse motivo, utilizo um código para automatizar e fazer boxplots para todas as 16 variáveis numéricas_.

---

### Célula 22
**Descrição**: _Primeiro OUTLIER identificado foi em relação ao QT_FILHOS que mostram 4 valores acima de 15. Como são poucos valores que se dispersam, iremos "apaga-los" posteriormente._.

---

### Célula 23
**Descrição**: _As variáveis QT_PC_PAGA_EM_DIA e QT_PARCELAS_PAGAS falam a respeito de parcelas de pagamento dos planos. Entretanto, o plano com maior duração ja visto anteriormente seria de 48 meses e nos boxplots é possível analisar que existem valores acima de 48, podendo ser um erro de digitação que teremos que corrigir depois nos tratamentos dos dados. Aqui temos um exemplo de OUTLIER_.

---

### Célula 24
**Descrição**: _Foi analisado que possuímos mais de 440 mil registros nesse DataFrame. Como apenas 5 registros no QT_FILHOS foram dispersos, iremos exclui-los pois não terá tanto impacto. Realizo um groupby nesta variável assim como fizemos nas categóricas e mostra os 4 valores 'anormais'_.

---

### Célula 25
**Descrição**: _Identifico os valores considerados como outliers_.

---

### Célula 26
**Descrição**: _realizo uma função para mostrar os registros que estão com esses valores 'anormais' de QT_FILHOS. Com esse print tenho acesso a todas as informações dos registros que constam esses outliers, assim como seu ID..._.

---
