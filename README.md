# Previsão de Chuva em São Carlos com Random Forest

Projeto desenvolvido para a disciplina SCC0230 — Inteligência Artificial.

---

# Objetivo

Prever se houve chuva em São Carlos utilizando dados meteorológicos históricos do Instituto Nacional de Meteorologia.

O problema foi tratado como:

* Aprendizado Supervisionado
* Classificação Binária

---

# Dataset

Fonte oficial:

[INMET - Dados Históricos](https://portal.inmet.gov.br/dadoshistoricos?utm_source=chatgpt.com)

## Dados utilizados

* Período: 2006–2025
* Dados horários da estação de São Carlos
* Dataset final diário com 6998 registros

## Tratamento realizado

* Padronização dos arquivos
* Remoção de valores inválidos
* Interpolação de dados faltantes
* Agregação horária → diária

---

# Modelo

Foi utilizado um **Random Forest Classifier** com:

```python
class_weight='balanced'
n_estimators=100
```

Motivos da escolha:

* Robustez
* Bom desempenho em dados tabulares
* Resistência a overfitting
* Importância das variáveis

---

# Resultados

## Acurácia

```text
0.84
```

## Variáveis mais importantes

* Umidade relativa
* Ponto de orvalho
* Radiação global
* Pressão atmosférica
* Temperatura do ar

---

# Tecnologias

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

# Como Executar

Instale as dependências:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn requests
```

Abra o notebook:

```bash
jupyter notebook
```

---

# Estrutura do Projeto

```text
.
├── Trabalho_IA.ipynb
├── dados_sao_carlos_unificados.csv
├── dados_sao_carlos_diario.csv
└── README.md
```

---

# Disciplina

SCC0230 — Inteligência Artificial
Universidade de São Paulo — Instituto de Ciências Matemáticas e de Computação
