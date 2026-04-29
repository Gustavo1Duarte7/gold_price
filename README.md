📑 Relatório do Projeto: Previsão de Preços do Ouro
1. Objetivo do Projeto
O objetivo foi desenvolver um modelo de Inteligência Artificial capaz de prever o preço de fechamento (Close) do ouro com base em indicadores diários de mercado (Abertura, Máxima, Mínima e Volume), utilizando bibliotecas de Machine Learning em Python.

2. Processamento e Limpeza (Data Prep)
Origem: Dataset histórico do Kaggle ("Gold Price Trends").

Tratamento: As datas foram convertidas para o formato padrão e os dados foram divididos em 80% para treino (onde o modelo aprende) e 20% para teste (onde o modelo é desafiado com dados novos).

Variáveis (Features): Open, High, Low, Volume.

Alvo (Target): Close.

3. Modelagem e Evolução
O projeto passou por duas fases principais para atingir a melhor precisão:

Fase 1 - Decision Tree (Árvore de Decisão):

Criamos uma árvore que toma decisões baseada em perguntas lógicas.

Resultado: Erro Médio Absoluto (MAE) de 6.30.

Diagnóstico: O modelo estava a "decorar" demais o passado (overfitting).

Fase 2 - Random Forest (Floresta Aleatória):

Evoluímos para uma floresta de 100 árvores trabalhando juntas.

Resultado: Erro Médio Absoluto (MAE) de 4.68.

Ganho: Uma redução de erro de aproximadamente 25% em relação ao primeiro modelo.

4. Análise de Qualidade (Resíduos)
Através do gráfico de resíduos, identificamos que:

O modelo é extremamente confiável para preços em patamares estáveis.

Em momentos de grandes picos de preço (volatilidade extrema), o modelo tende a ter uma variação de erro maior (heterocedasticidade), o que é esperado em mercados financeiros.

5. Conclusão Final
O modelo de Random Forest provou ser a ferramenta mais robusta para este dataset, conseguindo prever o valor do ativo com uma margem de erro muito baixa. Este projeto demonstra o ciclo completo de um cientista de dados: desde a importação do CSV até a validação gráfica dos erros.
