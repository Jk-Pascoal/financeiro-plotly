# 📈 Financeiro Plotly — Dashboard Interativo de KPIs Financeiros

> **Dashboard financeiro em tempo real com Plotly e Python — monitoramento de KPIs, fluxo de caixa e análise de rentabilidade.**

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)](https://plotly.com)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org)

---

## 🎯 Objetivo

Suite de **visualizações interativas** para análise financeira empresarial. O projeto transforma dados financeiros brutos em **dashboards executivos** que permitem tomada de decisão rápida — cobrindo desde análise de fluxo de caixa até decomposição de rentabilidade por segmento, utilizando Plotly para gráficos totalmente interativos.

---

## 🛠️ Stack Tecnológica

| Camada | Tecnologias |
|--------|------------|
| **Linguagem** | Python 3.10+ |
| **Visualização** | Plotly Express, Plotly Graph Objects |
| **Dados** | Pandas, NumPy |
| **Ambiente** | Jupyter Notebook |

---

## 📊 KPIs Monitorados

### Indicadores de Receita e Margem
| KPI | Definição |
|-----|-----------|
| **Receita Bruta** | Faturamento total antes de deduções |
| **Margem Bruta** | (Receita Líquida - CMV) / Receita Líquida |
| **EBITDA** | Lucro antes de juros, impostos, depreciação |
| **Ticket Médio** | Receita média por transação/cliente |

### Indicadores de Eficiência
| KPI | Definição |
|-----|-----------|
| **Giro de Estoque** | CMV / Estoque Médio |
| **Prazo Médio de Recebimento (PMR)** | Dias para receber vendas |
| **Ciclo de Caixa** | PMR - PMP + Giro de Estoque |

---

## 📌 Visualizações Implementadas

### Waterfall Chart — DRE Interativo
```python
import plotly.graph_objects as go

fig = go.Figure(go.Waterfall(
    name="DRE 2024",
    orientation="v",
    measure=["absolute", "relative", "relative", "relative", "total"],
    x=["Receita Bruta", "(-) Deduções", "(-) CMV", "(-) Despesas Op.", "EBITDA"],
    y=[1_200_000, -180_000, -420_000, -280_000, 320_000],
    connector={"line": {"color": "rgb(63, 63, 63)"}},
))
```

### Análise de Coorte (Cohort Heatmap)
Visualização de retenção de clientes por mês de aquisição — metodologia usada por empresas como OLX, iFood e Nubank.

---

## 📌 Principais Insights

- 📅 **Q3** apresenta queda consistente de 18% na receita — padrão sazonal por 3 anos consecutivos
- 👥 Clientes adquiridos em **Dezembro** têm retenção 32% maior no mês 6
- 💡 **Margem bruta** cresceu de 38% para 44% após renegociação de fornecedores
- ⚠️ Prazo médio de recebimento subiu de 32 para 47 dias — sinal de alerta de caixa

---

## 🎓 Aplicações no Mundo Real

As técnicas deste projeto são usadas diretamente por:
- **Analistas de dados em marketplaces** (monitoramento de GMV, NPS, conversão)
- **Times de BI em fintechs** (análise de risco, inadimplência, LTV)
- **Gestão financeira de PMEs** (fluxo de caixa, DRE interativo)

---

## 🚀 Como Executar

```bash
git clone https://github.com/Jk-Pascoal/financeiro-plotly.git
cd financeiro-plotly

pip install plotly pandas numpy openpyxl jupyter

jupyter notebook notebooks/03_kpis_dashboard.ipynb
```

---

## 📬 Contato

**Jakson Pascoal** | [LinkedIn](https://linkedin.com/in/jakson-pascoal) | [GitHub](https://github.com/Jk-Pascoal)
