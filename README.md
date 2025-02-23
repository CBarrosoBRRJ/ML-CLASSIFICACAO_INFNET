# Análise de Qualidade de Vinhos

Este projeto tem como objetivo analisar a qualidade de vinhos brancos e tintos com base em suas características físico-químicas. Utilizamos técnicas de machine learning para classificar os vinhos como "bons" ou "ruins" e comparar o desempenho dos modelos em diferentes conjuntos de dados.

---

## Descrição do Projeto

O conjunto de dados contém informações sobre vinhos brancos e tintos, incluindo características como acidez, pH, teor alcoólico, entre outras. A variável alvo é a qualidade do vinho, que foi transformada em uma variável binária (`opiniao`), onde:
- `0`: Vinho ruim (qualidade <= 5)
- `1`: Vinho bom (qualidade > 5)

O projeto segue as seguintes etapas:
1. **Pré-processamento dos dados**:
   - Tratamento de valores faltantes.
   - Codificação de variáveis categóricas.
   - Separação dos dados em vinhos brancos e tintos.

2. **Treinamento de modelos**:
   - Foram testados três modelos de classificação: Regressão Logística, Árvore de Decisão e SVM.
   - Utilizamos validação cruzada estratificada com k-folds (k=10) para avaliar o desempenho dos modelos.

3. **Otimização de hiperparâmetros**:
   - Usamos `GridSearchCV` para encontrar os melhores hiperparâmetros para cada modelo.

4. **Avaliação dos modelos**:
   - Calculamos métricas como acurácia, precisão, recall e F1-score.
   - Geramos curvas ROC para comparar o desempenho dos modelos.

5. **Inferência em novos dados**:
   - Aplicamos o melhor modelo (SVM) aos dados de vinho tinto para prever a qualidade dos vinhos.

---

## Resultados

### Desempenho do Melhor Modelo (SVM)
- **Acurácia**: 92.18%
- **Precisão**: 93.04%
- **Recall**: 92.28%
- **F1-Score**: 92.66%

O modelo SVM apresentou o melhor desempenho, com alta acurácia e um bom equilíbrio entre precisão e recall.

### Comparação entre Vinhos Brancos e Tintos
O modelo treinado com vinhos brancos generalizou bem para os vinhos tintos, com métricas de desempenho semelhantes.

---
