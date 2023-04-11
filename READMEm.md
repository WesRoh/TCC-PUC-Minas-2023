# APLICAÇÃO DE MACHINE LEARNING PARA A
PREVISÃO DE TENDÊNCIAS AÇÕES DA PETROBRÁS

--<br><br>
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white) <br>
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)<br>

--

# Introdução
PUC MINAS 2023
Este projeto apresenta um estudo de *machine learning* para realizar predições no preço de ações da PETROBRÁS na bolsa de valores.<br>
A ideia é que ao fechamento do pregão sabemos como foi no decorrer de um peiodo. 

---
# O Problema 
O problema proposto consiste na construção de um algoritmo para auxiliar na tomada de decisão de compra de ações na bolsa de valores B3. O trabalho não deve ser visto como a construção de uma metodologia para definir a compra, mas sim uma ferramenta que apoia a decisão baseada em dados históricos da ação da Petrobras 'PETR4'.
---

# Desenvolvimento

## Obtendo e tratando os dados

Foram usadas duas fontes de dados distintas, uma contendo dados históricos do valor da ação e outra contendo dados históricos do valor do dólar. A seguir são apresentados os métodos de captura da informação e uma breve descrição dos dados obtidos.Para o desenvolvimento deste trabalho foi utilizada a biblioteca Pandas, PyCaret  e a API do Yahoo Finance (YAHOO, 2023). Dessa forma, um dataset contendo o histórico do valor das ações pode ser obtido com facilidade. O uso da API Yahoo Finance pode ser feito conforme o código a seguir, aplicado à ação da Petrobras (PETR4) para o período 01/01/2013 a 01/01/2023.
A biblioteca **Pandas** foi utilizada para a manipulação de dados dentro do *dataframe*, para remover e acrescentar dados, enquanto a biblioteca **yfinance** foi utilizada para acessar os dados das ações da Petrobrás disponíveis no site **Yahoo Finance**.<br>

## Criando o modelo de *machine learning*

Dividimos o dataframe original em dois, criando um dataframe contendo os últimos 253 dias de pregão para que testássemos o desempenho de previsão do algoritmo com estes dados de fechamento.<br>
Utilizamos a biblioteca **PyCaret** para configurar os dados para treinamento e comparamos as métricas de acurácia dos diferentes modelos de regressão disponíveis na biblioteca de regressão do Pycaret.<br>
Após observarmos que o modelo **Bayesian Ridge** obteve as melhores métricas de acurácia diante dos outros testados pelo Pycaret, realizamos um *tuning* para melhorar ainda mais as métricas de acurácia e fizemos um último teste com os dados de treinamento para ver como o modelo se comportava.<br>
Por fim, pudemos plotar gráficos relevantes e fazer as predições dos preços dos últimos 253 pregões da PETR4. A biblioteca **Plotly** foi utilizada para plotar o gráfico final de comparação entre os preços de fechamento da PETR4 e os preços previstos pelo modelo.

---

# Conclusão

Em conclusão, a utilização da biblioteca PyCaret tem sido uma ferramenta valiosa para a Ciência de Dados. Com sua interface intuitiva e ampla gama de recursos, PyCaret permite que os usuários construam modelos de aprendizado de máquina de forma rápida e eficiente, mesmo sem uma compreensão profunda de programação e estatística.
Além disso, a biblioteca oferece suporte para uma ampla variedade de tarefas de aprendizado de máquina, desde classificação até clustering e regressão. Isso torna PyCaret uma escolha versátil para cientistas de dados que trabalham em projetos de diferentes domínios.


---

----

## Author:
**Weslei Rodrigo**
