# Regressão Linear - Projeção de Preços

## Data Science Project - Projeção de Preços

<div align='center'>

![ecommerce](https://github.com/caiomichelan/linear_regression-price_prediction/assets/104601836/eb31a5f9-d6b3-45df-9935-511049157e6c)

</div>

# 1. Problema do Negócio
<p align='justify'>Uma empresa de E-Commerce que atua no ramo de Moda com roupas, calçados e acessórios vem apresentando um crescimento exponencial nos últimos anos e consequentemente expandindo seu estoque, identificando a necessidade de otimizar os preços de seus produtos visando a maximização dos lucros com as vendas.</p>
<p align='justify'>Foi avaliado pela Diretoria Financeira que o sistema de precificação atual está configurado de uma maneira ineficaz, ocasionando problemas de subprecificação e sobreprecificação em diversos produtos recentemente cadastrados, já que se trata de um sistema único a todos os produtos, sendo que nem todas as categorias de produtos apresentam o mesmo comportamento em relação às vendas.</p>
<p align='justify'>Diante deste desafio, o objetivo principal é implantar uma nova etapa de precificação que considera que os preços dos produtos deverão ser otimizados com base em suas características, utilizando como base os preços históricos de produtos já registrados pela empresa.</p>

# 2. Premissas do Negócio
<p align='justify'>Foram desconsiderados fatores externos como economia e segmento do negócio.</p>
<p align='justify'>Dados nulos foram descartados da base histórica.</p>


# 3. Estratégia da Solução
<p align='justify'>Foi utilizada a metodologia CRISP-DM no desenvolvimento do projeto, através das seguintes etapas:</p>
<p align='justify'>- Data Description: Adquirir conhecimento sobre os dados com análise de colunas e sua nomenclatura, dimensão, tipos, verificação de dados nulos bem como seu tratamento e análise estatística descritiva a fim de encontrar padrões em suas métricas básicas. Nesta etapa também foi realizada a quebra dos dados da coluna “product_details” que estavam encapsulados.</p>
<p align='justify'>- Exploratory Data Analysis: Realização de análise exploratória para identificação de padrões e melhor entendimento das variáveis e sua relevância ao aprendizado do modelo estatístico. Nesta etapa foram realizadas análises univariadas, bivariadas e multivariadas, com dados númericos e categóricos. Foram definidas as hipóteses voltadas ao negócio e através das análises bivariadas as referidas hipóteses foram validadas.</p>
<p align='justify'>- Feature Engineering: Realizada a transformação dos dados categóricos em númericos com técnicas de Encoding.</p>
<p align='justify'>- Data Filtering: Filtro nos dados a fim de considerar os dados mais relevantes para a análise e modelagem estatística. Nesta etapa não foram realizados filtros, mas foi definida a remoção de algumas colunas que não tiveram relevância na elaboração do modelo.</p>
<p align='justify'>- Data Preparation: Preparação dos dados para aplicação dos modelos de Machine Learning, onde foram utilizadas técnicas de Rescaling e Transformation.</p>
<p align='justify'>- Feature Selection: Seleção das melhores variáveis a serem consideradas para treinamento do modelo de Machine Learning. A princípio foi utilizado o Boruta para apoio na seleção, mas após análise das variáveis consideradas foi avaliado que algumas variáveis excluídas neste processo também tinham relevância ao treinamento do modelo. Desta forma foram consideradas todas as variáveis selecionadas pelo Boruta e adicionadas outras variáveis manualmente. Também foram removidas as variáveis que não possuem nenhuma relevância ao treinamento do modelo.</p>
<p align='justify'>- Machine Learning Modelling: Realizado o treinamento de alguns modelos de Machine Learning com base nos dados propostos com a comparação de suas performances e avaliação do modelo ideal a ser utilizado efetivamente no projeto. Nesta etapa foram avaliados os modelos Gradient Boost Regressor, Random Forest Regressor, LGBM Regressor e por fim o Voting Regressor, o qual foi implementado pela possibilidade de extrair o melhor resultado dos outros modelos em conjunto.</p>


# 4. Insights de Dados
<p align='justify'>Algumas hipóteses validadas através da Análise Exploratória dos Dados:</p>
<p align='justify'>Hipóteses de Produtos no escopo de suas características:</p>
<p align='justify'>- Produtos com cores básicas estão em maiores quantidades (Hipótese Aceita);</p>
<p align='justify'>- Produtos com cores básicas possuem em média o menor preço (Hipótese Rejeitada);</p>
<p align='justify'>- Produtos de algodão possuem preços abaixo da média (Hipótese Aceita);</p>
<p align='justify'>- Produtos com padrão sólido possuem preço abaixo da média (Hipótese Rejeitada);</p>
<p align='justify'>- Categorias de vestuário possuem em média os maiores preços (Hipótese Aceita).</p>
<p align='justify'>Também foram observados Insights importantes, conforme segue:</p>
<p align='justify'>- Ao todo foram identificadas 301 marcas diferentes de produtos;</p>
<p align='justify'>- Foram identificadas 3 categorias de produtos, sendo Roupas e Acessórios, Calçados e Bolsas, Carteiras e Cintos;</p>
<p align='justify'>- Foram identificadas 23 sub categorias de produtos;</p>
<p align='justify'>- A maioria dos produtos é feita de Algodão (74%);</p>
<p align='justify'>- A maioria dos produtos consiste em Moda Ocidental (68,8%);</p>
<p align='justify'>- A maioria dos produtos atendem ao público Masculino (61,5%);</p>
<p align='justify'>- A maioria dos produtos tem a India como país de origem (40,2%).</p>

# 5. Produto Final
<p align='justify'>Com base nos dados históricos dos produtos e suas características, foi desenvolvido um modelo de projeção de preços a cada produto individualmente, visando auxiliar efetivamente na definição da correta precificação dos novos produtos cadastrados.</p>

# 6. Conclusão
<p align='justify'>O objetivo do projeto foi desenvolver um modelo de projeção de preços aos novos produtos cadastrados, garantindo que não ocorram problemas de subprecificação ou sobreprecificação, já que o novo modelo considera a projeção de cada produto individulamente com base em suas características.</p>
<p align='justify'>Com a implementação do modelo foi possível realizar a projeção individual dos preços aos produtos com uma margem média de erro de aproximadamente 10%, o que pode garantir uma precificação sem perda considerável no volume de vendas, consequentemente maximizando o lucro à empresa.</p>
<p align='justify'>Com base na projeção apresentada, a Diretoria Financeira poderá prosseguir com a precificação dos novos produtos de maneira eficiente.</p>

# 7. Próximos Passos
<p align='justify'>Como próximos passos serão definidos estudos voltados às características geográficas dos consumidores de modo a avaliar a correta precificação com base em sua região, bem como orientar análises voltadas ao frete através da demanda de transporte dos produtos.</p>
<p align='justify'>Também serão realizados estudos para otimização do modelo em produção com base nas necessidades da diretoria.</p>
