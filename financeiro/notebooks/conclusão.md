# 💰 Análise Financeira Estratégica com Python e Power BI

Este projeto tem como objetivo explorar dados de movimentações financeiras (recebimentos e pagamentos) para identificar **padrões críticos**, **tendências temporais**, **comportamentos regionais**, e **oportunidades de otimização do fluxo de caixa**.

Unindo a **flexibilidade do Python (para tratamento estatístico e visualizações avançadas)** com a **acessibilidade do Excel** e a **clareza do Power BI para dashboards executivos**, entregamos uma análise completa, estruturada e de valor estratégico.

---

## 📁 Sobre os Dados

- **Base:** Dados financeiros com transações de **pagamentos** e **recebimentos** por município, loja, forma de pagamento e data.  
- **Total de transações:** 'R$49.739.026,02' 
- **Período analisado:** `02/01/2020` até `28/12/2021`
- 
- **Colunas principais:**
  - `data da movimentação`
  - `tipo` (Pagamento ou Recebimento)
  - `valor da movimentação`
  - `município`
  - `forma pagamento`
  - `nome` (Loja)

---

## 🎯 Objetivo da Análise

Responder perguntas estratégicas como:

- Quais municípios concentram os maiores valores de movimentações?
- Como o volume financeiro evolui ao longo do tempo?
- Quais formas de pagamento são mais utilizadas em recebimentos e pagamentos?
- Existem outliers que merecem atenção?
- Há discrepâncias entre o número de lojas e volume financeiro por município?
- Quais são os bancos mais utilizados para cada tipo de movimentação?
- Existem lojas com movimentações anormais?

---

## 🧪 Etapas do Projeto

### 1. Tratamento de Dados
- Renomeação e padronização de colunas
- Conversão de tipos (ex: `category`, `datetime`)
- Exclusão de colunas irrelevantes
- Identificação e tratamento de outliers com IQR
- Verificação de valores nulos e duplicados

### 2. Análises Exploratórias (EDA)

#### 📍 Municípios em Destaque
- **São Paulo** lidera com 29% dos recebimentos e apenas 12% dos pagamentos.
- **Belo Horizonte** tem o maior volume de **pagamentos**, mesmo gerando menos receita que outras cidades.
- **Vitória** tem muitas lojas (25%) mas movimentação financeira baixa, indicando possível baixa performance.

#### 📊 Volume Financeiro Total
- **Valor total movimentado:** R$49.739.026,02
- **Recebimentos:** 68% do total
- **Lucro estimado:** R$9.739.026,02

#### ⏳ Evolução Temporal
- Picos de movimentações ocorrem geralmente no **meio do ano** e **início de cada ano**
- Tendência relativamente estável com variações sazonais

#### 💳 Formas de Pagamento
- **PIX** é o mais utilizado para **recebimentos** (50%)
- **Cartão** lidera nos **pagamentos** (48%), seguido por PIX (40%)
- Juntos, representam 88% de todas as transações de pagamento

#### 🏦 Instituições Financeiras
- **Pagamentos:** Nubank (45%) e Itaú (35%) → 80% das transações
- **Recebimentos:** Itaú (34%) e Nubank (26%) → 61% das transações
- **Bradesco** é o menos utilizado (3% nos pagamentos)

#### ⚠️ Outliers
- Transações de **pagamentos** chegando a quase **R$8 milhões**
- **Recebimentos** com valores elevados próximos de **R$6 milhões**
- Loja **"Notaro Paulista"** com destaque em pagamentos (R$866 mil)
- Recomendado: investigação dos valores fora do padrão

---

## 📈 Visualizações Criadas

- Gráfico de barras por tipo de movimentação
- Top 10 municípios por valor total de recebimentos
- Boxplot por tipo de movimentação
- Linhas temporais com evolução mensal
- Barras com frequência e valor por forma de pagamento
- Evolução temporal por tipo de pagamento (ex: Pix, Cartão, Boleto)

---

## 📊 Dashboard no Power BI

> **Em desenvolvimento.**  
O dashboard incluirá:

- Resumo financeiro geral
- Análise temporal comparativa
- Preferências de meios de pagamento
- Mapa por município
- Lojas com movimentações anormais

---

## 📌 Conclusão Executiva

- **São Paulo** se destaca positivamente com **alta receita e baixo custo**
- **Belo Horizonte** tem alto volume de saída e merece atenção
- **PIX e Cartão** dominam as transações, com alta aceitação
- Nubank e Itaú concentram a maior parte das movimentações
- Algumas cidades com muitas lojas têm desempenho abaixo do esperado
- Há outliers financeiros relevantes que exigem investigação

---

## 🧠 Aprendizados

Este projeto me ajudou a:

- Consolidar o uso de `pandas`, `seaborn` e `matplotlib`
- Aplicar conceitos de **estatística descritiva**
- Trabalhar com **séries temporais**
- Estruturar análises financeiras com lógica de negócio
- Criar **visuais estratégicos** para facilitar a tomada de decisão
- Praticar a escrita analítica para stakeholders

---
rojeto em andamento. Feedbacks são bem-vindos!
