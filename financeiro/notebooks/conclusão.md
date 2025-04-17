# 💰 Análise Financeira Estratégica 

Este projeto tem como objetivo explorar dados de movimentações financeiras (recebimentos e pagamentos) para identificar **padrões críticos**, **tendências temporais**, **comportamentos regionais**, e **oportunidades de otimização do fluxo de caixa**.

Unindo a **flexibilidade do Python (para tratamento estatístico e visualizações avançadas)** com a **acessibilidade do Excel** e a **clareza do Power BI para dashboards executivos**, entregamos uma análise completa, estruturada e de valor estratégico, os dados utilizados para a analálise foram retirados do kaglle.

---

## 📁 Sobre os Dados

- **Base:** Dados financeiros com transações de **pagamentos** e **recebimentos** por município, loja, forma de pagamento e data.  
- **Total de transações:** 'R$49.739.026,02' 
- **Período analisado:** `02/01/2020` até `28/12/2021`
- 
- **Colunas principais:**
  - `data da movimentação`: data em que foi realizada as movimentações.
  - `tipo`: Coluna mostra que tipo de movimentação foi feita, se ela foi Recebimento ou Pagamento.
  - `valor da movimentação`: Mostra qual valor foi o Pagamanto ou o Recebimento.
  - `município`: Mostra os municípios onde esta localizado cada loja.
  - `forma pagamento`: que forma de pagamento foi utilizada
  - `nome`:Informa os nomes das

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

## conclusões tirada da análise  
## 
## 📍 Análise: Quais municípios concentram os maiores valores de movimentações?

### 📌 Dados observados:
- **São Paulo** lidera em **recebimentos**, com **29%** do total da receita da empresa.
- Possui apenas **13%** dos **pagamentos**, mesmo concentrando **27%** das lojas.

### 🔎 Interpretação:
Essa diferença entre entrada e saída indica uma **eficiência financeira acima da média**. São Paulo demonstra ser o município mais **rentável**, equilibrando bem operação e resultado.

### ✅ Recomendações:
- Utilizar São Paulo como **referência operacional**.
- Considerar o município como prioridade em decisões de **expansão ou investimento futuro**.

---
## Como o volume financeiro evolui ao longo do tempo?
## 📍 Análise: Evolução do volume financeiro em 2020

### 📌 Dados observados:
- Crescimento nos recebimentos de **janeiro a março**, especialmente no **Rio de Janeiro**, que manteve alta até abril.
- **Vitória** e **Belo Horizonte** tiveram picos isolados em apenas **um mês**.
- Após **junho**, os valores caíram e se mantiveram **instáveis** até o fim do ano.
- **São Paulo** foi o único município a manter **picos recorrentes** durante o ano.

### 🔎 Interpretação:
A **performance nacional em 2020** foi impulsionada principalmente por São Paulo e Rio de Janeiro. A instabilidade no segundo semestre sugere necessidade de monitoramento de sazonalidades.

### ✅ Recomendações:
- **Investir em estratégias comerciais** para os meses mais fracos.
- Estudar os motivos da **queda pós-junho** e desenvolver **ações preventivas** para períodos semelhantes em anos futuros.

---

## 📍 Análise: Comparativo entre 2020 e 2021

### 📌 Dados observados:
- **2021** teve performance inferior a 2020.
- Apenas um pico significativo em **setembro (R$13 milhões)**.
- Receitas totais: **R$53 milhões em 2020** vs **R$41 milhões em 2021** (queda de **22%**).

### 🔎 Interpretação:
A empresa perdeu força em 2021, com menos variação positiva e volume financeiro menor. Isso pode indicar retração do mercado ou necessidade de ajustes operacionais.

### ✅ Recomendações:
- Analisar o contexto de mercado em 2021.
- Avaliar **ações de marketing ou operacionais** que possam ter impactado negativamente.
- Criar estratégias para **recuperar o crescimento observado em 2020**.

---

## 📍 Análise: Formas de pagamento mais utilizadas

### 📌 Dados observados:
- Nos **recebimentos**, o **PIX** representa **50%**, seguido por **cartão (22%)**.
- Nos **pagamentos**, o **cartão lidera com 48%**, seguido por **PIX (40%)**.

### 🔎 Interpretação:
O PIX é a principal escolha dos clientes na hora de pagar, indicando preferência por **transações rápidas e de baixo custo**.

### ✅ Recomendações:
- **Otimizar os canais de recebimento via PIX**, garantindo agilidade e estabilidade.
- **Explorar promoções para pagamentos à vista**, reforçando esse comportamento.
- **Monitorar tendências** de preferência dos clientes para adaptar a estratégia de cobrança e pagamento.

## 🔍 Dado Observado: Outliers em Recebimentos e Pagamentos

Durante a análise dos dados financeiros, foram identificados **outliers significativos** tanto nas entradas (recebimentos) quanto nas saídas (pagamentos).

- **Recebimentos**: observou-se que existem transações que se aproximam de **R$6 milhões**, enquanto o **terceiro quartil (Q3)** está abaixo de **R$1 milhão**, evidenciando uma alta dispersão nos valores.
- **Pagamentos**: há registros que chegam próximos de **R$9 milhões**, sendo que a maior parte dos outliers está na faixa de **R$3 milhões**, também acima do Q3 (em torno de R$1 milhão).

### 📈 Interpretação

Esses valores destoam significativamente do padrão da maioria das movimentações. Eles podem estar relacionados a **lojas com transações atípicas**, seja por porte diferenciado, localização estratégica ou sazonalidade.

- No caso dos **pagamentos**, valores tão elevados podem indicar **endividamentos expressivos**, **investimentos de grande porte** ou **compromissos operacionais pontuais**.
- Já nos **recebimentos**, essas movimentações extremas podem estar associadas a **clientes corporativos**, **grandes campanhas promocionais** ou **transações com alto valor agregado**.

> ⚠️ A falta de informações detalhadas sobre a natureza de cada transação impede uma análise totalmente conclusiva. No entanto, a diferença em relação ao comportamento médio é evidente e merece atenção.

### 🎯 Recomendação

É altamente recomendado investigar mais profundamente a **origem dessas movimentações**, a fim de compreender se elas representam:

- **Riscos financeiros** (como dívidas elevadas ou desequilíbrios operacionais)
- Ou **oportunidades comerciais** (grandes receitas, contratos vantajosos)

**Sugestões práticas**:

- Revisar contratos e transações específicas associadas às lojas envolvidas
- Avaliar se os pagamentos altos são eventos pontuais ou recorrentes
- Considerar a segmentação dos dados por tipo de operação (investimento, despesa, pagamento de fornecedores, etc)

---

## 📍 Análise por Município: Lojas vs Volume Financeiro

### 🧾 Dados Observados

- A quantidade de lojas por cidade é **relativamente equilibrada**, com **São Paulo** possuindo **27%** das unidades.
- O volume de **recebimentos** segue um padrão semelhante, com São Paulo acumulando **29%** do total.
- Já os **pagamentos** apresentam uma **discrepância significativa**:
  - **Belo Horizonte**: 34%
  - **Vitória** e **Rio de Janeiro**: ~26% cada
  - **São Paulo**: apenas 13%

### 💡 Interpretação

Apesar de ter um número levemente maior de lojas, São Paulo gera a **maior parte das receitas** com a **menor parte dos pagamentos**, destacando-se como uma **cidade altamente rentável**.

> ✅ Este comportamento indica que São Paulo é um modelo de **eficiência operacional**, podendo servir como benchmark para as demais localidades.

### ✅ Recomendações

- **Explorar novos mercados** com perfil semelhante ao de São Paulo
- **Investigar a operação em Belo Horizonte**, que apresenta altos pagamentos
- **Avaliar a performance individual das lojas** nas cidades com maior volume de despesas

---

## 🏦 Bancos Mais Utilizados em Transações

### 📑 Dados Observados

- **Recebimentos**: 61% realizados via **Itaú e Nubank**
- **Pagamentos**: 80% realizados por essas mesmas instituições

### 🔍 Interpretação

A predominância de Itaú e Nubank indica:

- Padronização operacional com foco em **eficiência e controle**
- Preferência de clientes e fornecedores por esses bancos
- Bons relacionamentos institucionais que podem gerar vantagens

### ✅ Recomendações

- **Negociar condições comerciais** com os bancos mais usados
- **Manter opções alternativas** para mitigar riscos operacionais
- **Investigar a experiência do cliente** com essas instituições para otimizar os meios de pagamento

---

## 🏪 Lojas com Movimentações Financeiras Anormais

### 📑 Dados Observados

**Recebimentos muito acima da média**:
- Nova Olinda B: R$ 12.129.777,06
- Indaia: R$ 8.123.600,57
- Elkem Carboderivados: R$ 7.053.013,70

**Pagamentos elevados**:
- Notaro Paulista: R$ 8.667.090,74 (acima da média de R$1M–R$3M)

### 🔍 Interpretação

- **Nova Olinda B** é uma unidade extremamente lucrativa
- **Notaro Paulista** apresenta gastos atípicos, podendo indicar investimentos, endividamentos ou desequilíbrios

### ✅ Recomendações

- Monitorar o desempenho de lojas como Nova Olinda B
- Investigar a fundo os pagamentos da Notaro Paulista
- Identificar se os gastos são estratégicos ou representam ineficiências

---

