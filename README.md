
# 📊 Projeto USP-IC-SIN5006 - Previsão de Séries Temporais com Modelos de Deep Learning

![Badge](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)  
![Badge](https://img.shields.io/badge/python-3.10-blue)  
![Badge](https://img.shields.io/badge/Deep%20Learning-TensorFlow%20%7C%20Keras%20%7C%20Sklearn-brightgreen)

---

## 🚀 **Descrição do Projeto**
Este projeto tem como objetivo implementar, treinar, comparar e analisar modelos de redes neurais aplicados à **previsão de séries temporais**, utilizando dados relacionados à geração de energia solar e variáveis climáticas da **Bacia Amazônica**.

Foram utilizados três tipos de modelos de aprendizado supervisionado:
- 🔷 **LSTM (Long Short-Term Memory)**
- 🔷 **GRU (Gated Recurrent Unit)**
- 🔷 **MLP (Perceptron Multi-Camadas)**

---

## 🎯 **Objetivo Principal**
- Avaliar o desempenho dos modelos na previsão de séries temporais.
- Comparar modelos em diferentes datasets, entendendo qual apresenta maior precisão, menor erro e maior robustez.
- Aplicar essas técnicas na área de previsão de energia renovável.

---

## 🏗️ **Estrutura do Projeto**
```
USP-IC-SIN5006/
│
├── notebooks/          → Notebooks de execução dos modelos e análises.
├── datasets/           → Bases de dados utilizadas no treinamento e teste.
├── outputs/            → Saída dos resultados (gráficos, CSVs, modelos).
├── README.md           → Documentação do projeto.
└── ...                 → Outros arquivos de apoio.
```
---

## ⚙️ **Pipeline Executado**
1. 🔍 **Pré-processamento:**
   - Normalização dos dados com `MinMaxScaler`.
   - Criação de janelas temporais (`look_back=30`).

2. 🧠 **Modelagem:**
   - Construção dos modelos LSTM, GRU e MLP.
   - Treinamento sobre os 12 datasets disponíveis.

3. 📊 **Avaliação:**
   - Cálculo de métricas:
     - **MAE** (Mean Absolute Error)
     - **RMSE** (Root Mean Squared Error)
     - **R²** (Coeficiente de Determinação)
     - **MAPE** (Mean Absolute Percentage Error) → ⭐️ *Adicionado para comparação percentual entre datasets.*

4. 📈 **Geração de Saídas:**
   - CSV com os valores de **Real** vs. **Previsto**.
   - Tabela consolidada de métricas.
   - Gráficos: MAE, RMSE, R² e MAPE.

---

## 🔎 **Interpretação dos Resultados**
- **Real:** Valor verdadeiro, registrado no dataset.
- **Previsto:** Valor calculado pelo modelo de machine learning.

### 📑 Interpretação das Métricas:
- **MAE:** Erro médio absoluto — quanto, em média, o modelo erra.
- **RMSE:** Dá mais peso aos grandes erros.
- **R²:** Mede o quão bem o modelo explica a variabilidade dos dados. Ideal = 1.
- **MAPE:** Erro percentual médio — útil para comparar datasets de diferentes escalas.

---

## 🏆 **Conclusões Técnicas**
- ✔️ **GRU** foi o modelo mais robusto, apresentando:
  - Menor MAE e RMSE na maioria dos datasets.
  - Maior R² e menor MAPE.
- ⚠️ **LSTM não teve desempenho satisfatório**, com altos erros e R² negativo em muitos datasets.
- 🔥 **MAPE se mostrou essencial** para comparar datasets com escalas distintas.

---

## 📊 **Dashboard Interativo**
Execute localmente o dashboard com:
```bash
pip install streamlit pandas plotly
streamlit run dashboard.py
```
Ou use o dashboard embutido nos notebooks com **Plotly Dash**.

---

## 🔥 **Resultados Disponíveis**
- ✔️ Notebooks completos e executáveis no Google Colab.
- ✔️ Dashboard interativo.
- ✔️ Gráficos de MAE, RMSE, R² e MAPE.
- ✔️ Apresentação em PowerPoint (`Apresentacao.pptx`).
- ✔️ Resultados em CSV (`outputs/`).

---

## 🧠 **Possíveis Melhorias Futuras**
- Ajuste fino dos hiperparâmetros (tuning).
- Aplicação de redes neurais híbridas (CNN + GRU, Attention, Transformers).
- Aplicação de técnicas de engenharia de atributos.
- Análise robusta de anomalias nos datasets.

---

## 👥 **Autores**
- 👨‍💻 Projeto desenvolvido no contexto da disciplina **USP-IC-SIN5006 - Inteligência Computacional**.
- **Testes feitos por:** rlcf - basedo no trabalho:
- Neural Networks Forecast Models Comparison for the Solar Energy Generation in Amazon Basin, ANDRÉ LUÍS FERREIRA MARQUES 1, MÁRCIO JOSÉ TEIXEIRA 2,FELIPE VALENCIA DE ALMEIDA 1, AND PEDRO LUIZ PIZZIGATTI CORRÊA1, 1 Polytechnic School, University of São Paulo, São Paulo 05508-010, Brazil, 2 Institute of Physics, University of São Paulo, Sao Pãulo 05508-090, Brazil.

---

## 📜 **Licença**
Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para mais detalhes.

---

## 🚀 **Status do Projeto**
✅ Concluído e funcional para execução, testes, análises e apresentações.
