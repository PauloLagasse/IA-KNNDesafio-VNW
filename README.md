# IA-KNN-Desafio-VNW

# Modelo de Classificação para Elegibilidade de Crédito

## Descrição

Este projeto contém um modelo de classificação baseado em KNN para prever a elegibilidade de solicitações de empréstimo/crédito em três categorias:

1. **Não Elegível** – Solicitações recusadas ou negadas.  
2. **Elegível com Análise** – Solicitações que precisam de análise mais detalhada.  
3. **Elegível** – Solicitações aprovadas imediatamente.

O modelo foi treinado com base nas seguintes variáveis (features): salário anual, total de dívidas, score de pagamento e crédito solicitado.

---

## Detalhes do Modelo

- **Tipo de modelo:** KNN (K-Nearest Neighbors)  
- **Valor de K:** 12  
- **Variáveis utilizadas:**  
  - `salario_anual`  
  - `total_dividas`  
  - `historico_pagamento (score)`  
  - `credito_solicitado`  
- **Ordem das variáveis na entrada do modelo:**  
  `[salario_anual, total_dividas, historico_pagamento (score), credito_solicitado]`

- **Observação**
  - A variável `idade` foi **ignorada**
---

## Normalização

Os dados foram normalizados usando o `StandardScaler` da biblioteca `sklearn.preprocessing`. O arquivo do scaler (`scaler_credito.joblib`) está fornecido para garantir que novas entradas sejam escalonadas corretamente antes da previsão.

---

## Exemplo de previsão

- **Entrada (X):** `[50000, 10, 0.85283, 5000]`  
- **Saída prevista (y):** `[2]`  
  - Onde 2 corresponde a categoria **Elegível com Análise**.
---

## Arquivos fornecidos

- `modelo_knn_credito.joblib` — arquivo do modelo KNN treinado.  
- `scaler_credito.joblib` — arquivo do scaler utilizado para normalização das variáveis.

---

## Significado das classes (target)

| Classe | Significado           |
|--------|----------------------|
| 1      | Não Elegível         |
| 2      | Elegível com Análise |
| 3      | Elegível             |
