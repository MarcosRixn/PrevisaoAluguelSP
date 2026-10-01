<h1 align="center">
  Previsão de aluguel de imóveis em São Paulo
</h1>

<p align="center">
  Projeto de Machine Learning para análise e previsão de preços de aluguel de imóveis no estado de São Paulo.
</p>

<p align="center">
 <a href="#objetivo">Objetivo</a> •
 <a href="#fonte">Dataset</a> •
 <a href="#analise">Análise Exploratória</a> •
 <a href="#modelo">Modelagem</a> •
 <a href="#resultados">Resultados</a> •
 <a href="#conclusao">Conclusão</a>
</p>

---

<h2 id="objetivo">🎯 Objetivo</h2>

<p>
Este projeto tem como objetivo desenvolver um modelo de Machine Learning capaz de estimar o valor de aluguel de imóveis em São Paulo a partir das características disponíveis no dataset.
</p>

<p>
Além da construção do modelo preditivo, o projeto contempla etapas de análise exploratória dos dados, pré-processamento, comparação entre algoritmos de regressão, validação cruzada e otimização de hiperparâmetros.
</p>

<h2 id="fonte">🗃️ Dataset</h2>

<p>
Os dados utilizados neste projeto foram obtidos no Kaggle, no dataset
<a href="https://www.kaggle.com/datasets/argonalyst/sao-paulo-real-estate-sale-rent-april-2019">
São Paulo Real Estate — Sale / Rent — April 2019
</a>.
</p>

<p>
O conjunto de dados original possui 16 variáveis relacionadas às características dos imóveis.
</p>

<p>
Inicialmente, foram identificadas:
</p>

<ul>
  <li>11 colunas do tipo inteiro;</li>
  <li>3 colunas do tipo string;</li>
  <li>2 colunas do tipo float;</li>
  <li>ausência de valores nulos nas variáveis analisadas.</li>
</ul>

<h2 id="analise">🔍 Análise Exploratória dos Dados</h2>

<p>
Durante a etapa de Análise Exploratória, foram avaliadas a distribuição das variáveis, suas características estatísticas e a correlação entre as features e a label <code>Price</code>.
</p>

<p>
Entre as principais etapas realizadas estão:
</p>

<ul>
  <li>análise dos tipos de dados;</li>
  <li>verificação de valores ausentes;</li>
  <li>análise da distribuição das variáveis por meio de histogramas;</li>
  <li>seleção e remoção de atributos considerados pouco relevantes para o objetivo da modelagem;</li>
  <li>análise da correlação entre as variáveis numéricas;</li>
  <li>identificação da variável <code>Size</code> como uma das features com maior correlação com <code>Price</code>.</li>
</ul>

<h2 id="modelo">🤖 Modelagem</h2>

<p>
Após a análise exploratória, foi realizado o pré-processamento dos dados para preparação das variáveis utilizadas pelos modelos.
</p>

<p>
A variável categórica <code>District</code> foi transformada utilizando <code>OneHotEncoder</code>, permitindo sua utilização pelos algoritmos de regressão.
</p>

<p>
Os dados foram posteriormente separados em conjuntos de treinamento e teste, reservando 30% das observações para a avaliação final do modelo.
</p>

<h3>Modelos avaliados</h3>

<ul>
  <li><code>LinearRegression</code></li>
  <li><code>DecisionTreeRegressor</code></li>
  <li><code>RandomForestRegressor</code></li>
</ul>

<p>
Os modelos foram comparados utilizando validação cruzada (<em>Cross Validation</em>) e uma métrica de erro para avaliar sua capacidade de generalização.
</p>

<p>
Entre os algoritmos avaliados, o <code>RandomForestRegressor</code> apresentou o melhor desempenho durante a validação cruzada e, por isso, foi selecionado.
</p>

<h3>Otimização de hiperparâmetros</h3>

<p>
Para melhorar o desempenho do modelo selecionado, foi utilizado o <code>GridSearchCV</code>, para diferentes combinações de hiperparâmetros e selecionar os melhores resultados.
</p>

<h2 id="resultados">📊 Resultados</h2>

<p>
Após a definição dos melhores hiperparâmetros, o modelo final foi treinado e avaliado sobre o conjunto de teste.
</p>

| Métrica | Resultado |
|---|---:|
| RMSE | `1813` |

<p>
Também foi realizada a comparação entre os valores reais dos imóveis e os valores estimados pelo modelo, permitindo avaliar visualmente o comportamento das previsões.
</p>

<h2 id="conclusao">💡 Conclusão</h2>

<p>
O projeto demonstrou a aplicação de um fluxo básico de Machine Learning para um problema de regressão, passando pelas etapas de análise exploratória, preparação dos dados, comparação de algoritmos, validação cruzada e otimização de hiperparâmetros.
</p>

<p>
Entre os modelos avaliados, o <code>RandomForestRegressor</code> apresentou o melhor desempenho para o conjunto de dados utilizado.
</p>

<p>
Apesar da quantidade limitada de atributos explorados neste projeto, os resultados demonstram o potencial do modelo para estimar valores de aluguel a partir das características disponíveis.
</p>

<h3>👨‍💻 Autor</h3>
<p>Marcos Rian</p>
