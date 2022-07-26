# Integrantes

Lucas Cardoso Lazari 8927439

Diogo José Costa Alves 13709881

Lucas de Angelis Oliveira 8989189

Thales Vinicius Gomes 9814265

# Descrição do dataset

Os dados a serem utilizados no projeto são provenientes de um estudo realizado em pacientes infectados por COVID-19 (doi.org/10.1080/20002297.2022.2043651). 
Neste estudo, o nível de proteínas em amostras de soro de pacientes internados e não internados por COVID-19 foram avaliados, portanto, o dataset consiste em 
uma série de features que correspondem a proteínas identificadas e um valor de intensidade da sua medida para cada paciente. A proposta do projeto é utilizar 
este dataset para treinar modelos para classificar os pacientes em alto risco (internados) ou baixo risco (não internados) baseado nos valores de intensidade 
das proteínas identificadas. São no total 132 amostras para treinamento/validação e 64 amostras para teste. Ambos os datasets (treino e teste) estão desbalanceados. 
O objetivo é melhorar o que foi feito no estudo publicado, visando aumentar a performance de classificação no dataset de teste.

# Plano de trabalho

1. Realização de uma análise exploratória no dataset com a finalidade de compreender as distribuições das variáveis, seus ranges de valores ou tipos (em caso de categórica), a correlação variável-variável e variável-feature, ou seja, ter uma melhor ideia dos dados que se está trabalhando. Neste etapa se usará amplamente bibliotecas Python de manipulação e análise de dados como Pandas, Numpy, Scipy, além de bibliotecas de visualização como MatplotLib e Seaborn.

2. Definição de qual métrica de performance iremos utilizar para validar a performance do modelo implementado. Dado que já foi publicado um artigo com uma certa performance (que podemos utilizar de baseline) as métricas serão definidas baseadas nessa comparação entre modelos.

3. Dado que o dataset já está dividido em treino e teste e a quantidade disponível de dados é pequena, é necessário determinar qual será a técnica utilizada para obtenção das métricas de validação (usadas para comparar diferentes modelagens e técnicas de tratamento e pré processamento). Para essa etapa podemos considerar algumas técnicas conhecidas como StratifiedKFold, RepeatedKFold, entre outras.

4. Testar tratamentos e pré processamentos para melhorar a performance do modelo. Tendo um dataset com poucos exemplos e com desbalanceamento entre classes, será possível testar técnicas de Under Sampling e Over Sampling (SMOTE, por ex). Nesta parte também será interessante testar métodos de inputação de dados para colunas com missing values (Simple Imputer, Iterative Imputer, KNN Imputer, Tree-Based Imputer, etc). Além disso também é importante determinar quais features são mais importantes, se existem features muito correlacionadas ou que não contribuem para o aprendizado que podem ser removidas.

5. Explorar modelos amplamente usados em dados tabulares e com possibilidade de busca extensiva de hiper parâmetros como LightGBM, XGBoost, TabNet, entre outros. Outra possibilidade é implementar um Voting Classifier (Soft ou Hard) com todos os modelos que foram treinados no artigo.

6. Determinar com base na performance em validação quais técnicas e modelos performaram melhor para a avaliação final no set de teste.
