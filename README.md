# 📊 Análise de Churn - TelecomX

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SAGIEV007/Analise-de-Churn-TelecomX/blob/main/Analise%20de%20Churn.ipynb)

## 🎯 Objetivo

Análise completa de dados de clientes da TelecomX para identificar padrões de evasão (churn) através de um processo estruturado de **ETL (Extract, Transform, Load)** e **EDA (Exploratory Data Analysis)**.

## 📋 Descrição do Projeto

A TelecomX enfrenta um alto índice de evasão de clientes. Este projeto realiza uma análise exploratória detalhada dos dados para identificar os principais fatores que levam à perda de clientes, fornecendo insights acionáveis para reduzir o churn.

### Dataset
- **Total de registros:** 7.267 clientes
- **Variáveis:** 22 atributos (demográficos, serviços, financeiros)
- **Fonte:** API TelecomX (GitHub)
- **Formato:** JSON estruturado

## 🚀 Como Usar

### Opção 1: Google Colab (Recomendado)
Clique no botão acima ou acesse diretamente:
``
https://colab.research.google.com/github/SAGIEV007/Analise-de-Churn-TelecomX/blob/main/Analise%20de%20Churn.ipynb
``
### Opção 2: Executar Localmente
``bash
# Clonar o repositório
git clone https://github.com/SAGIEV007/Analise-de-Churn-TelecomX.git
cd Analise-de-Churn-TelecomX

# Instalar dependências
pip install pandas numpy matplotlib seaborn requests

# Executar o notebook
jupyter notebook "Analise de Churn.ipynb"
``

## 📊 Estrutura do Notebook

### 1. **📌 Extração (Extract)**
- Carregamento automático dos dados da API TelecomX
- Validação e exploração inicial dos dados
- Verificação de estrutura e quantidade de registros

### 2. **🔧 Transformação (Transform)**
- Normalização de dados JSON em DataFrame estruturado
- Conversão de tipos de dados
- Tratamento de valores ausentes
- Feature engineering (grupos de tenure, contagem de serviços)

### 3. **📊 Análise (Load & EDA)**
- **8 visualizações profissionais:**
  - Distribuição de churn
  - Análise demográfica (gênero, idade, parceiro, dependentes)
  - Análise de serviços (internet, telefone, adicionais)
  - Análise financeira (charges mensais e totais)
  - Análise de tenure (tempo de cliente)
  - Matriz de correlação

### 4. **💡 Insights e Recomendações**
- Taxa de churn por segmento
- Fatores críticos de risco
- 5 recomendações estratégicas
- Conclusões e próximos passos

## 🔑 Principais Insights

| Fator | Impacto | Observação |
|-------|--------|-----------|
| **Tipo de Contrato** | Alto | Mês-a-mês tem 5x mais churn que 2 anos |
| **Tenure** | Alto | Primeiros 12 meses são críticos |
| **Charges Mensais** | Médio | Clientes com charges altos tendem a fazer mais churn |
| **Tipo de Internet** | Médio | Fiber Optic tem padrão diferente |
| **Serviços Adicionais** | Médio | Mais serviços = menor churn |

## 📈 Recomendações Estratégicas

1. **Programa de Retenção para Novos Clientes**
   - Onboarding robusto nos primeiros 12 meses
   - Incentivos para upgrade de contrato
   - Acompanhamento proativo

2. **Revisão de Estratégia de Preços**
   - Análise de custo-benefício
   - Pacotes com melhor valor
   - Descontos para contratos de longo prazo

3. **Melhoria de Qualidade de Serviço**
   - Foco em qualidade de internet
   - Melhor suporte técnico
   - Serviços adicionais de valor

4. **Segmentação de Clientes**
   - Segmentos de risco
   - Estratégias direcionadas
   - Ofertas personalizadas

5. **Monitoramento Contínuo**
   - Dashboard em tempo real
   - KPIs de retenção
   - Análises periódicas

## 📊 Variáveis Analisadas

### Demográficas
- `customerID` - Identificador único
- `gender` - Gênero
- `SeniorCitizen` - Cidadão sênior (0/1)
- `Partner` - Tem parceiro (Yes/No)
- `Dependents` - Tem dependentes (Yes/No)

### Serviços
- `PhoneService` - Serviço de telefone
- `MultipleLines` - Múltiplas linhas
- `InternetService` - Tipo de internet (DSL, Fiber optic, No)
- `OnlineSecurity` - Segurança online
- `OnlineBackup` - Backup online
- `DeviceProtection` - Proteção de dispositivo
- `TechSupport` - Suporte técnico
- `StreamingTV` - TV por streaming
- `StreamingMovies` - Filmes por streaming

### Conta
- `Contract` - Tipo de contrato (Month-to-month, One year, Two year)
- `PaperlessBilling` - Fatura sem papel
- `PaymentMethod` - Método de pagamento
- `MonthlyCharges` - Charges mensais
- `TotalCharges` - Total de charges

### Derivadas
- `tenure` - Meses como cliente
- `tenure_group` - Grupo de tenure
- `charges_group` - Grupo de charges
- `num_internet_services` - Número de serviços
- `Churn` - Indicador de evasão (0/1)

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Pandas** - Manipulação de dados
- **NumPy** - Computação numérica
- **Matplotlib** - Visualizações
- **Seaborn** - Gráficos estatísticos
- **Requests** - Requisições HTTP
- **Google Colab** - Ambiente de execução

## 📁 Estrutura do Repositório

``
Analise-de-Churn-TelecomX/
├── Analise de Churn.ipynb          # Notebook principal
├── README.md                         # Este arquivo
├── INSTRUCOES_NOTEBOOK.md           # Guia detalhado
└── TelecomX_Data.json               # Dataset (opcional)
``

## 📚 Referências

- [Pandas Documentation](https://pandas.pydata.org/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Matplotlib Documentation](https://matplotlib.org/)
- [Google Colab Guide](https://colab.research.google.com/)
- [Desafio Alura ONE](https://www.alura.com.br/)

## 💾 Exportação de Dados

O notebook gera automaticamente dois arquivos CSV:

1. **telecom_dados_tratados.csv** - Dataset completo tratado
2. **telecom_resumo_estatistico.csv** - Resumo estatístico

## 🔄 Fluxo de Dados

``
API TelecomX (JSON)
        ↓
   Extração
        ↓
   Normalização
        ↓
   Limpeza & Transformação
        ↓
   DataFrame Pandas
        ↓
   Análise Exploratória
        ↓
   Visualizações & Insights
        ↓
   Exportação CSV
``

## 📞 Próximos Passos

Após completar esta análise, você pode:

1. **Desenvolver Modelos Preditivos**
   - Usar Machine Learning para prever churn
   - Classificadores: Logistic Regression, Random Forest, XGBoost

2. **Criar Dashboard Interativo**
   - Visualizar métricas em tempo real
   - Monitorar KPIs de retenção

3. **Implementar Estratégias**
   - Ações baseadas em dados
   - Programas de retenção direcionados

4. **Validar Resultados**
   - A/B testing de estratégias
   - Medir impacto nas taxas de churn

## ⚙️ Requisitos

- Python 3.7+
- Bibliotecas: pandas, numpy, matplotlib, seaborn, requests
- Acesso à internet (para carregar dados da API)
- Google Colab (recomendado) ou Jupyter Notebook local

## 📝 Notas Importantes

- O notebook carrega dados automaticamente da API TelecomX
- Todas as transformações são documentadas no código
- Os gráficos são gerados automaticamente durante a execução
- Os dados são exportados em CSV para análises futuras

## 🎓 Conclusão

Esta análise fornece uma base sólida para entender os padrões de churn na TelecomX. Com os insights gerados, a equipe de Data Science pode desenvolver estratégias mais eficazes para reduzir a evasão de clientes e melhorar a retenção.

---

**Desenvolvido para o Desafio de Data Science - Alura ONE**

**Autor:** Análise de Dados Automatizada

**Data:** Dezembro 2025

**Status:** ✅ Completo e Pronto para Uso
