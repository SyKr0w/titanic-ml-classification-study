Predição de Sobrevivência no Titanic – Comparação de Modelos

  Este projeto desenvolve e compara três modelos de classificação supervisionada (SVC, Random Forest e XGBoost) para prever a sobrevivência de passageiros do Titanic com base em dados tabulares.

*Objetivos
 - Construir modelos capazes de prever sobrevivência (0 ou 1).
 - Comparar desempenho usando ROC-AUC como métrica principal.
 - Avaliar custo computacional entre os algoritmos.
 - Aplicar boas práticas de pré-processamento e validação cruzada.

*Pré-Processamento
 - Tratamento de valores ausentes:
 - Idade substituída pela mediana.
 - Porto de embarque pela moda.
 - Escalonamento de variáveis numéricas (age, fare).
 - Codificação One-Hot das variáveis categóricas.
 - Divisão estratificada entre treino e teste.
 - Uso de random_state=42 para reprodutibilidade.

*Modelos Utilizados
 - SVC (Kernel RBF) – bom para fronteiras não lineares.
 - Random Forest – modelo de árvores robusto e estável.
 - XGBoost – algoritmo de boosting eficiente.

 Todos passaram por otimização com RandomizedSearchCV e validação StratifiedKFold (5 folds).

*Resultados Gerais
 - Random Forest e XGBoost se destacaram no desempenho.
 - XGBoost teve o treinamento mais rápido.
 - Houve leve overfitting em todos os modelos, esperado dado o tamanho reduzido do dataset.
 - A generalização permaneceu satisfatória.

*Como Reproduzir
 - Abrir o notebook “Atividade_Final_de_Inteligência_Artificial.ipynb”.
 - Executar as células em ordem.
 - A validação, métricas e comparações são mostradas no próprio notebook.

*Conclusão
  O projeto demonstra como diferentes algoritmos de classificação se comportam no problema clássico do Titanic, reforçando a importância do pré-processamento, da validação cruzada e da seleção criteriosa de modelos.