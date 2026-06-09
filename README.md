# 🏠 Previsão de Preço de Casas - Regressão Linear Múltipla

[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.2-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📌 Sobre o Projeto

Este projeto implementa um modelo de **Regressão Linear Múltipla** para prever o preço de casas utilizando o dataset **California Housing**. O objetivo é entender como diferentes variáveis influenciam o preço dos imóveis e interpretar os resultados do modelo.

**Dataset:** California Housing (Scikit-learn)

## 🎯 Objetivos

- Construir um modelo de regressão linear múltipla
- Calcular e interpretar métricas de avaliação (MAE, MSE, R²)
- Analisar os coeficientes das variáveis
- Identificar quais variáveis mais influenciam o preço
- Visualizar previsões vs valores reais

## 📊 Principais Resultados

### Métricas do Modelo

| Métrica | Valor | Interpretação |
|---------|-------|----------------|
| MAE (Erro Absoluto Médio) | 0.5332 | Erro médio de ~US$ 53.320 |
| MSE (Erro Quadrático Médio) | 0.5559 | Penaliza erros grandes |
| R² (Coeficiente de Determinação) | 0.5758 | 57,6% da variação é explicada |

### Coeficientes das Variáveis

| Variável | Coeficiente | Interpretação |
|----------|-------------|----------------|
| AveBedrms | +0.7831 | Mais quartos por dormitório → preço mais alto |
| MedInc | +0.4487 | Maior renda da região → preço mais alto |
| HouseAge | +0.0097 | Casas mais antigas → preço ligeiramente maior |
| Longitude | -0.4337 | Regiões mais a leste → preço mais baixo |
| Latitude | -0.4198 | Regiões mais ao norte → preço mais baixo |
| AveRooms | -0.1233 | Efeito contraintuitivo (possível multicolinearidade) |

## 🔍 Principais Insights

### 1. Variáveis que mais aumentam o preço
- **AveBedrms (Média de quartos por dormitório)**: cada aumento de 1 unidade → +US$ 78.310
- **MedInc (Renda média)**: cada aumento de 1 unidade → +US$ 44.870
- **HouseAge (Idade da casa)**: efeito positivo, mas muito pequeno (+US$ 970 por ano)

### 2. Variáveis que mais diminuem o preço
- **Longitude/Latitude**: localização é crucial - regiões costeiras do sul da Califórnia são mais caras
- **AveRooms**: resultado contraintuitivo que pode indicar multicolinearidade com AveBedrms

### 3. Qualidade do Modelo
- R² de 0.5758 é **bom para dados imobiliários** (muitos fatores subjetivos não capturados)
- MAE de ~US$ 53.320 é razoável considerando a faixa de preços (US$ 15.000 - US$ 500.000)

## 📈 Visualização

O gráfico de previsões vs valores reais mostra que:
- O modelo captura a tendência geral dos dados
- Há dispersão considerável (modelo não é perfeito)
- Para preços muito altos (>US$ 500.000), o modelo tende a subestimar

## 🛠️ Tecnologias Utilizadas

- Python 3.8+
- Pandas (manipulação de dados)
- NumPy (operações numéricas)
- Matplotlib & Seaborn (visualizações)
- Scikit-learn (modelagem e métricas)


## 🚀 Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/projeto-preco-casas.git
cd projeto-preco-casas
```

2. Instale as dependências:
```bash
pip install -r requirements.txt
```

3. Execute o Jupyter Notebook:
```bash
jupyter notebook preco_casas_regressao.ipynb
```

## Aprendizados
- O R² de 0.5758 indica que 57,6% da variação dos preços é explicada pelas variáveis do modelo
- MedInc (renda média) é um dos fatores mais importantes para preço de imóveis
- Localização (Latitude/Longitude) tem forte impacto negativo quando a casa está mais ao norte/leste
- O coeficiente negativo de AveRooms foi uma surpresa, possivelmente devido à multicolinearidade com AveBedrms
- Modelos lineares funcionam bem, mas têm limitações para capturar relações não-lineares

## 📚 Referências
- California Housing Dataset - Scikit-learn
- Scikit-learn Documentation

👨‍💻 Autora
Kailayni Rodrigues Janez - @KailayniJanez
