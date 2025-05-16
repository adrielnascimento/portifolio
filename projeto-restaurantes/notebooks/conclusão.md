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

# 📍 Conclusões e Recomendações

### Quais bairros têm mais restaurantes?

**📊 Dados:**  
Entre os 30 bairros analisados, Byresandra, Tavarekere e Madiwala se destacam com 798 restaurantes — o que representa 11% do total (7.105). Logo em seguida, vem Bannerghatta Road, com 552 restaurantes (7%).

**🔍 Interpretação:**  
A distribuição de restaurantes pelos bairros é relativamente equilibrada, ou seja, não existe uma concentração absurda em poucas regiões. Isso mostra uma boa dispersão da oferta. Por outro lado, alguns bairros aparecem pouco representados.

**💡 Recomendação:**  
Vale investigar por que locais como Residency Road, com apenas 18 restaurantes, têm tão pouca presença. Pode ser por estrutura limitada, baixa demanda ou outros fatores. Entender isso ajuda a traçar boas estratégias pra expansão em áreas que ainda estão “em branco” no mapa gastronômico.

## 📍 Bairros com mais restaurantes

![Bairros com mais restaurantes](https://raw.githubusercontent.com/adrielnascimento/portifolio/main/projeto-restaurantes/notebooks/imagem/qdt_restaurantes_bairro.png)


---

### Quais os tipos de cozinha mais comuns?

**📊 Dados:**  
Muitos restaurantes oferecem mais de um tipo de cozinha, mas alguns estilos lideram. As combinações North Indian, Chinese (421 restaurantes), North Indian (420) e South Indian (348) dominam, somando cerca de 60% do total.

**🔍 Interpretação:**  
A culinária indiana — do norte e do sul — é disparada a preferida. Isso reflete os hábitos locais e talvez uma demanda forte por esses sabores mais tradicionais.

**💡 Recomendação:**  
Quem tá pensando em abrir um restaurante pode apostar nesses estilos pra atrair o público mais rápido. Mas também dá pra pensar fora da caixa: oferecer culinárias menos comuns (como japonesa, italiana, etc.) pode chamar atenção de nichos ainda pouco explorados e gerar diferencial.


---

### Quais os tipos de cozinha com mais avaliações (e melhores notas)?

**📊 Dados:**
- North Indian: 52.717 avaliações – média 3,4  
- North Indian, Chinese: 40.010 – média 3,3  
- South Indian: 35.963 – média 3,4  

**🔍 Interpretação:**  
Esses três estilos de cozinha são os mais comentados e bem avaliados, o que mostra popularidade e presença de mercado. As notas giram entre 3,3 e 3,4, o que indica um nível de satisfação consistente, mas não espetacular.

**💡 Recomendação:**  
A demanda por essas culinárias é real, então vale manter ou incluir essas opções no cardápio. E como as notas ainda têm margem pra crescer, investir em atendimento, qualidade e experiência pode ser o diferencial pra sair da média e entrar no top da galera.

---

### Tipo de restaurante influencia na nota?

**📊 Dados:**
Bares e pubs são os campeões de nota, beirando os 5 pontos. Microcervejarias também mandam bem, geralmente com média acima de 4. Nenhum tipo de restaurante teve média abaixo de 3.

**🔍 Interpretação:**  
O público curte muito a experiência nesses tipos de lugar, o que sugere que ambiente e proposta contam bastante na hora de avaliar. A consistência nas notas mostra que a qualidade tá num nível bom no geral.

**💡 Recomendação:**  
Vale olhar mais de perto o que esses bares e pubs estão fazendo de certo — pode ser o ambiente, o atendimento, o cardápio... Entender isso pode ajudar outros tipos de restaurante a melhorarem a experiência do cliente e, de quebra, subirem nas avaliações.

---

### Como estão distribuídas as avaliações?

**📊 Dados:**
O que os dados mostram:
A maioria das avaliações vai de 3 a 4 pontos. Cerca de 25% dos restaurantes têm nota igual ou inferior a 3.2. A mediana é 3.5, e 75% das notas estão abaixo de 3.8.

Inter
**🔍 Interpretação:**  
O panorama geral é positivo — poucas notas muito baixas. Mas existem exceções, com avaliações bem ruins (abaixo de 2.5) e outras excelentes (acima de 4.5). Isso mostra uma certa variação na experiência dos clientes.

**💡 Recomendação:**  
É bom ficar de olho nos casos com notas muito baixas. Ver o que tá dando errado (atendimento? comida? ambiente?) pode ajudar a fazer ajustes pontuais e melhorar a percepção geral dos clientes.

## 📍 Distribuição das avalições

![Distribuição das avalições](https://raw.githubusercontent.com/adrielnascimento/portifolio/main/projeto-restaurantes/notebooks/imagem/dis_av_restaurantes.png)

---
![Distribuição das avalições](https://raw.githubusercontent.com/adrielnascimento/portifolio/main/projeto-restaurantes/notebooks/imagem/distribuição_av_restaurantes.png)

---

### Quais restaurantes cobram mais caro?

**📊 Dados:**
Os três restaurantes com os maiores valores médios para duas pessoas são:

Le Cirque Signature – The Leela Palace: R$6.000 (French, Italian)

Royal Afghan – ITC Windsor: R$5.000 (North Indian, Mughlai)

Malties – Radisson Blu: R$4.500 (Continental, Fast Food)

Enquanto isso, metade dos restaurantes cobra menos de R$400, e 75% cobram menos de R$600. Ou seja, esses três são claramente voltados pra um público mais exclusivo.

**🔍 Interpretação:**  
Eles são outliers, atuando em um nicho premium — e, por isso, a expectativa do cliente também sobe junto com a conta.


**💡 Recomendação:**  
Se cobram caro, têm que entregar uma experiência à altura. Investir em ambiente, atendimento, apresentação e divulgação voltada ao público de luxo é essencial. E claro: monitorar as avaliações pra garantir que o valor está sendo justificado.

---

### Cozinhas específicas se concentram em certos bairros?

**📊 Dados:**  
 - Os tipos de cozinha mais comuns (North Indian, South Indian, North Indian + Chinese) aparecem na maioria dos bairros. Mas em alguns locais, um tipo específico domina com folga.
   
**🔍 Interpretação:**  
Isso pode ser reflexo de preferências locais ou até mesmo de falta de variedade nas opções.


**💡 Recomendação:**  
Pode ser uma boa oportunidade testar novos tipos de culinária em regiões onde há pouca diversidade. Além disso, cruzar dados de localização + avaliação pode ajudar a entender onde faz sentido apostar em novidades.

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
