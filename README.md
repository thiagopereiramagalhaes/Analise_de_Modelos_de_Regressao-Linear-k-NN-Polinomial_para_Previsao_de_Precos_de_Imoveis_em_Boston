# Análise e Previsão de Preços de Imóveis em Boston

## 1. O que é este projeto?

Este projeto tem como objetivo principal analisar e prever o valor médio das propriedades na região de Boston, nos Estados Unidos. A previsão de preços no mercado imobiliário é um desafio clássico que ajuda tanto compradores quanto vendedores, bem como investidores e planeadores urbanos, a tomarem decisões mais informadas sobre o valor justo de uma habitação.

Para alcançar este objetivo, o projeto explora uma base de dados ("Boston Housing") com informações detalhadas sobre várias características de diferentes zonas da cidade — como a taxa de criminalidade, a acessibilidade às autoestradas, o número médio de divisões por casa, e os níveis de poluição, entre outros fatores socioeconómicos e ambientais. Com base nestas características, o projeto procura criar e comparar diferentes modelos de Inteligência Artificial (especificamente, modelos de regressão) para perceber qual deles consegue estimar de forma mais precisa e fiável o preço final das casas.

Em suma, este projeto resolve o problema da incerteza na avaliação imobiliária, ajudando a traduzir dados complexos e multifatoriais da cidade em estimativas de valor de mercado que qualquer pessoa sem conhecimento técnico consegue compreender.

## 2. Como o fiz?

O desenvolvimento do projeto decorreu de forma estruturada e em várias etapas para garantir a transparência e a precisão dos resultados. Todo o trabalho foi desenvolvido em linguagem Python, utilizando um formato de documento interativo (*Jupyter Notebook*), seguindo as boas práticas da ciência de dados:

1. **Recolha de Dados:** Utilizámos a famosa base de dados "Boston Housing", que contém 506 registos históricos com 14 características iniciais de habitações e localidades em Boston.
2. **Análise e Exploração dos Dados:** Primeiramente, observámos as características dos dados para entender a sua distribuição. Recorremos a estatísticas descritivas e criámos gráficos visuais (como diagramas de dispersão e gráficos de caixas ou *boxplots*) para identificar tendências e anomalias de forma clara.
3. **Limpeza e Tratamento da Informação:**
    * Eliminámos a variável 'b' da base de dados (que correspondia à proporção de cidadãos negros por localidade), uma vez que se determinou que esta informação não seria utilizada para a modelagem dos preços.
    * Inspecionámos a base de dados em busca de eventuais dados nulos ou em falta, garantindo a qualidade da informação que iria alimentar os modelos preditivos.
4. **Preparação para a Modelação:**
    * **Separação de Dados (Holdout):** Dividimos a informação total em duas partes: um conjunto para "treinar" a máquina (para que aprenda os padrões de preços) e um conjunto isolado para "testar" a máquina (para avaliar a eficácia do algoritmo perante dados que este nunca viu).
    * **Normalização:** Ajustámos a escala dos valores numéricos de forma a garantir que todas as características fossem avaliadas de forma equilibrada pelos algoritmos.
5. **Treino e Avaliação de Modelos:** Para prever o valor das propriedades, construímos e ensinámos três modelos matemáticos distintos:
    * **Regressão Linear:** O método mais simples, que procura estabelecer uma linha de tendência direta entre as características da casa e o seu preço final.
    * **Algoritmo k-NN (k-Vizinhos Mais Próximos):** Um modelo que prevê o preço de uma casa com base na observação dos preços das casas "vizinhas" com as características mais semelhantes.
    * **Regressão Polinomial:** Um método mais avançado concebido para detetar padrões curvos e complexos que a linha reta não consegue captar.

Por fim, o projeto foca-se na comparação do desempenho destas três abordagens matemáticas distintas para determinar qual é a mais fiável e exata na previsão de preços de imóveis.
