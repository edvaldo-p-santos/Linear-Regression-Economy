# Linear Regression - Economy
Nesse projeto eu aplico duas regressões lineares utilizando a biblioteca "stats model" regredindo uma métrica de liberdade econômica em desemprego e renda per capita.

Um debate quente ultimamente com toda essa polarização é sobre os benefícios da liberdade econômica de um país. 
Perguntas como:

*  É bom privatizar as empresas?

*  O governo deve intervir na economia?

Diante essas perguntas quero mostrar algumas modelos de regressão que fiz e avaliar a relação de liberdade econômica e o PIB per capita e taxa de desemprego de um país. 

Quando acabar de ler esse post tenho certeza que você vai estar bem melhor para encarar aquela discussão no churrasco da família (ou não, rs). 

Vem comigo!


## Dados

### Índice de Liberdade Econômica
Os dados sobre liberdade econômica foi retirado de um índice calculado pela Fraser Institute. Esse índice mensura o quanto as políticas e as instituições do país serve de suporte para a liberdade econômica. 

A Fraser se debruçou sobre 5 abordagens para calcular esse índice:


1.   Tamanho do Governo
2.   Sistema Legal e Direito de Propriedade
3.   Moeda Forte
4.   Liberdade para Trocas Internacionais
5.   Regularização

Vou deixar o link ![aqui](https://www.fraserinstitute.org/studies/economic-freedom-of-the-world-2019-annual-report) para caso você queira se aprofundar. Te encorajo fortemente, pois vou deixar esse espaço para mostrar os resultados principalmente sem focar muito na teoria.

### **PIB per capita e Desemprego**

Peguei os dados do PIB per capita e desemprego por meio do site do FED (Sistema de Reserva Federal dos Estados Unidos).

OBS: Todos os dados foram coletados para o ano de 2016.

## Modelos para estimação:

𝑝𝑖𝑏=𝛽0+𝛽1∗𝑓𝑟𝑒𝑒𝑑𝑜𝑚
 
𝑡𝑥𝑑𝑒𝑠𝑒𝑚𝑝𝑟𝑒𝑔𝑜=𝛽0+𝛽1∗𝑓𝑟𝑒𝑒𝑑𝑜𝑚

## Resultados Regressão PIB ~ Liberdade
O modelo estimado é
pib = -7.4734 + 1.2846 x freedom

O que indica uma **correlação positiva** entre a liberdade econômica e PIB per capita. 

Pelos resultados notamos também que o R2 ~ 0.1.
Um valor não tão alto. O que indica um grau de ajuste não tão bom. Mas, como estamos pensando em inferência, não é um grande problema. Pelo P-valor (0.000) nota se que o parâmetro de 'freedom' é estatisticamente relevante.

## Resultados Regressão Tx. Desemprego ~ Liberdade
O modelo estimado é
txdesemp = 18.1 -1.4392 x freedom

O que indica uma **correlação negativa** entre liberdade econômica e taxa de desemprego. Então, um aumento na liberdade geraria menos desemprego.

Pelos resultados notamos também que o R2 ~ 0.062.
Um valor não tão alto. O que indica um grau de ajuste não tão bom. Contudo, pelo P-valor nota se que o parâmetro de 'freedom' é estatisticamente relevante a 0.9%.

## Conclusões

Nossos modelos deu um ajuste muito baixo e devemos ser cautelos em tomar uma conclusão. Provavelmente temos problema de especificação dos dados, ainda existe muitas outras variáveis que afetam essas variáveis dependentes. Mas, a partir deles notamos que liberdade econômica é bom para aumentar riqueza per capita e um menor desemprego. Nos dois modelos os parâmetros são estatisticamente significantes, o que nos leva a crer que a relação é coerente. 7

Sempre bom lembrar que há um outro lado da moeda. Maior eficiência é inversamente proporcional a igualdade, algo muito importante também. Logo, embora maior liberdade econômica gera maior produto e renda, mas não quer dizer que o ideal é ser totalmente livre!


Até mais!

