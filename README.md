# 📊 Análise de Churn - Projeto TelecomX

## 🔹 Objetivo
Este projeto tem como objetivo analisar a evasão de clientes (churn) da base de dados **TelecomX** e identificar fatores que contribuem para a saída dos clientes. Além disso, propomos estratégias de retenção baseadas nos resultados.

---

## 🔹 Base de Dados
Os dados utilizados foram previamente limpos e estão disponíveis em CSV:

- Contém informações demográficas, de contrato e de consumo dos clientes.
- Principais colunas:
  - `gender` – gênero do cliente
  - `contract` – tipo de contrato (mensal, anual, bienal)
  - `paymentmethod` – método de pagamento
  - `internetservice` – tipo de internet contratada
  - `chargesmonthly` – valor mensal
  - `chargestotal` – valor total gasto
  - `tenure` – tempo de contrato em meses
  - `churn` – indicador de evasão (0 = não, 1 = sim)

---

## 🔹 Pré-processamento
- Variáveis categóricas transformadas em numéricas usando **one-hot encoding**.
- Valores nulos foram tratados ou removidos.
- Análise de desbalanceamento das classes (churn):
  - Clientes ativos: 73.46%
  - Clientes evadidos: 26.54%
- Técnicas aplicadas para balanceamento:
  - Undersampling  
  - Oversampling  
  - SMOTE (geração de exemplos sintéticos)

---
## 🔹 Modelos Aplicados
1. **Regressão Logística**
   - Necessita normalização das features
   - Permite interpretar coeficientes das variáveis
2. **Random Forest**
   - Não requer normalização
   - Calcula a importância das variáveis para previsão

Outros modelos exploratórios:
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

---

## 🔹 Resultados e Insights
- Principais variáveis que influenciam churn:
  - Tempo de contrato (tenure)
  - Total gasto (chargestotal)
  - Tipo de contrato e método de pagamento
  - Presença de parceiro ou dependentes
- Estratégias de retenção recomendadas:
  - Incentivar contratos anuais com descontos
  - Monitorar clientes de baixo gasto e propor planos personalizados
  - Programas de fidelidade para clientes sem parceiro ou idosos
  - Promoções de serviços premium, especialmente para clientes de fibra óptica

---

## 🔹 Relatório Final
O relatório completo está disponível em PDF, contendo gráficos, tabelas de coeficientes e variáveis importantes.

- HTML estilizado: `/content/tmp/relatorio_churn_final.html`  
- PDF gerado: `/content/tmp/relatorio_churn_final.pdf`

---

