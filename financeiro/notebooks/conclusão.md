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
- São Paulo demonstrou um desempenho notável em comparação aos demais municípios, com alto volume de recebimentos e baixos níveis de saída, evidenciando eficiência financeira nas operações da região. Além disso, embora concentre um número levemente superior de lojas, essa diferença não é expressiva o suficiente para justificar, por si só, a superioridade nos resultados o que reforça a efetividade operacional das unidades presentes no município.
![Gráfico retratando o desempenho de São Paulo](financeiro/imagens/grafico1.png)
  -essa analise levantou a seguinte questão, qual loja que esta gerando os maiores valores de entrada pra São Paulo?
  -A análise dos recebimentos por loja em São Paulo revela que a unidade "Nova Olinda B" é a principal responsável pelos valores de entrada na região. Ela registrou um total expressivo de R$121.129.777,06, destacando-se significativamente em relação às demais lojas.

