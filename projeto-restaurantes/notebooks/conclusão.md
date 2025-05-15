# 🧠 Da Cozinha ao Cliente: Uma Análise Baseada em Dados da Zomato

## 📌 Introdução

Neste projeto, o foco é transformar dados em decisões estratégicas para o setor gastronômico. Utilizando o conjunto de dados da plataforma Zomato, disponível no Kaggle, realizamos uma análise completa para entender os principais fatores que impactam as avaliações dos restaurantes e a experiência dos usuários.

A proposta é simples, mas poderosa: extrair insights valiosos que se traduzem em recomendações práticas, ajudando restaurantes a melhorar sua performance, atrair mais clientes e conquistar melhores avaliações.

Todo o processo foi conduzido em **Python**, utilizando o **VS Code** como ambiente de desenvolvimento e bibliotecas robustas como `pandas`, `numpy`, `matplotlib` e `seaborn`. Foram realizadas etapas de limpeza e tratamento dos dados, seguidas por uma análise exploratória detalhada. Ao final, os dados tratados estão disponíveis para download neste mesmo diretório.

---

## 🧾 Sobre a Base de Dados – Zomato (Índia)

O dataset contém informações sobre restaurantes registrados na plataforma Zomato, incluindo localização, tipo de cozinha, avaliações e custo médio para duas pessoas.

- **Total de registros**: ~7.100 restaurantes  
- **Localidade**: Índia (com foco em cidades como Bangalore, Delhi, Hyderabad, entre outras)  
- **Período das avaliações**: Não especificado (dados atualizados no momento da coleta)

**Colunas principais:**

- `nome_restaurante`: Nome do estabelecimento  
- `tipo_cozinha`: Tipos de culinária oferecida  
- `tipo_restaurante`: Categoria (ex: Casual Dining, Café, etc.)  
- `avaliacao_5_pontos`: Nota média dos usuários (escala de 0 a 5)  
- `num_avaliacoes`: Quantidade de avaliações recebidas  
- `custo_medio_2_pessoas`: Custo estimado para duas pessoas  
- `bairro`: Localização aproximada  
- `tem_entrega`: Se o restaurante oferece delivery  
- `tem_reserva`: Se aceita reservas antecipadas  

---

## 🎯 Objetivo da Análise

Responder perguntas estratégicas e gerar recomendações com base em evidências dos dados:

- Quais bairros concentram a maior quantidade de restaurantes?  
- Quais os tipos de cozinha mais presentes?  
- Quais estilos culinários têm mais avaliações e melhores notas?  
- Existe relação entre o tipo de restaurante e sua avaliação média?  
- Como se distribuem as avaliações dos estabelecimentos?  
- Quais são os restaurantes com maior custo médio?  
- Há concentração de certas culinárias em bairros específicos?  

---

## 🛠️ Etapas do Projeto – Dataset Zomato

### 1. Tratamento de Dados

✔️ Renomeação e padronização das colunas  
✔️ Conversão de tipos (`int`, `float`, `category`)  
✔️ Exclusão de colunas irrelevantes  
✔️ Tratamento de outliers com IQR  
✔️ Verificação e tratamento de nulos e duplicados  

---

### 2. Análise Exploratória (EDA)

#### 🍽️ Total de Restaurantes
- A base contempla **7.105 restaurantes** cadastrados em Bangalore.

#### 🏙️ Bairros com maior concentração
- **Byresandra, Tavarekere, Madiwala**: 798 restaurantes (11%)  
- **Bannerghatta Road**: 552 restaurantes (7%)  
- **Brookefield**: 477 restaurantes (6%)  

#### 🍔 Tipos de Estabelecimentos mais comuns
- **Quick Bites**: 2.840 restaurantes (39%)  
- **Casual Dining**: 1.934 restaurantes (27%)  
- **Café**: 403 restaurantes (6%)  

#### 🍛 Culinárias mais populares
- **North Indian, Chinese** – 421 restaurantes  
- **North Indian** – 420 restaurantes  
- **South Indian** – 348 restaurantes  

> A culinária indiana (nas variações North e South) domina amplamente o cenário.

#### ⭐ Distribuição das Avaliações
- 1º Quartil (Q1): 3.2  
- Mediana (Q2): 3.5  
- 3º Quartil (Q3): 3.8  

> A maioria dos estabelecimentos possui avaliações entre **3.2 e 3.8**, indicando uma média estável.

#### 📝 Mais avaliados
- **Byg Brewski Brewing Company** – 16.345 avaliações  
- **Toit** – 14.956 avaliações  
- **The Black Pearl** – 10.413 avaliações  

#### 💰 Mais caros (custo médio p/ 2 pessoas)
- **Le Cirque Signature – The Leela Palace**: R$6.000  
- **Royal Afghan – ITC Windsor**: R$5.000  

---

### 3. Outliers e Recomendações

#### ⚠️ Outliers detectados
- Restaurantes com mais de **50.000 avaliações** e custos acima de **₹6.000** foram destacados como casos fora da curva.
- Alguns registros apresentam **avaliações baixas com preços elevados**, indicando inconsistências ou oportunidades de revisão de estratégia.

#### 🧠 Recomendações com base nos dados
- Investir em **serviços de entrega online e reservas**: há correlação entre essas opções e melhores avaliações.  
- Explorar **culinárias menos saturadas**, porém bem avaliadas, pode ser uma vantagem competitiva.  
- Monitorar outliers pode revelar **erros de cadastro** ou necessidade de **realinhar preços com a experiência entregue**.  

---

## 📍 Conclusões e Recomendações

### Quais bairros têm mais restaurantes?

**📊 Dados:**  
- Byresandra, Tavarekere, Madiwala: 798 restaurantes (11%)  
- Bannerghatta Road: 552 restaurantes (7%)

**🔍 Interpretação:**  
A distribuição é relativamente equilibrada, mas há bairros com presença mínima de restaurantes.

**💡 Recomendação:**  
Explorar regiões pouco atendidas como Residency Road pode ser uma boa estratégia de expansão.

---

### Quais os tipos de cozinha mais comuns?

**📊 Dados:**  
- North Indian, Chinese (421)  
- North Indian (420)  
- South Indian (348)

**🔍 Interpretação:**  
A culinária indiana domina o cenário, refletindo o gosto local.

**💡 Recomendação:**  
Apostar em estilos tradicionais pode ser seguro, mas investir em culinárias alternativas pode atrair nichos.

---

### Quais os tipos de cozinha com mais avaliações (e melhores notas)?

**📊 Dados:**
- North Indian: 52.717 avaliações – média 3,4  
- North Indian, Chinese: 40.010 – média 3,3  
- South Indian: 35.963 – média 3,4  

**🔍 Interpretação:**  
São os estilos mais populares e com desempenho estável nas avaliações.

**💡 Recomendação:**  
Apostar nessas culinárias, mas com foco em **melhorar qualidade e experiência**, pode elevar as notas.

---

### Tipo de restaurante influencia na nota?

**📊 Dados:**
- Bares e pubs: médias próximas de **5**
- Microcervejarias: média acima de **4**

**🔍 Interpretação:**  
Ambiente e proposta têm impacto direto na avaliação.

**💡 Recomendação:**  
Outros restaurantes podem aprender com o sucesso desses estabelecimentos para melhorar a experiência.

---

### Como estão distribuídas as avaliações?

**📊 Dados:**
- 25% ≤ 3.2  
- Mediana: 3.5  
- 75% ≤ 3.8  

**🔍 Interpretação:**  
Notas são medianas para a maioria, mas há exceções nos extremos.

**💡 Recomendação:**  
Focar nos restaurantes com notas muito baixas e entender os motivos pode melhorar a imagem geral.

---

### Quais restaurantes cobram mais caro?

**📊 Dados:**
- Le Cirque Signature – R$6.000  
- Royal Afghan – R$5.000  
- Malties – R$4.500  

**🔍 Interpretação:**  
Estes são nichos premium. A expectativa dos clientes é alta.

**💡 Recomendação:**  
É essencial entregar **experiência de alto padrão** para justificar os preços.

---

### Cozinhas específicas se concentram em certos bairros?

**📊 Dados:**  
- Culinárias como North Indian estão presentes em vários bairros.

**🔍 Interpretação:**  
Algumas regiões são dominadas por um estilo só, o que pode indicar falta de variedade.

**💡 Recomendação:**  
Apostar em **diversidade gastronômica em bairros mais homogêneos** pode ser uma vantagem estratégica.

---

## 📎 Conclusão

Esse projeto mostra como uma análise de dados bem feita pode trazer insights práticos e aplicáveis para o mercado de alimentação. A partir da base da Zomato, conseguimos mapear padrões de consumo, avaliar preferências regionais e sugerir estratégias reais para restaurantes se destacarem.

---

### 📂 Arquivos

- `zomato_data_tratado.csv`: Dados limpos e prontos para uso  
- `notebook.ipynb`: Análises e visualizações  
- `README.md`: Documentação e explicações do projeto (esse arquivo!)

---

### 🚀 Ferramentas utilizadas

- Python  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- VS Code

---
