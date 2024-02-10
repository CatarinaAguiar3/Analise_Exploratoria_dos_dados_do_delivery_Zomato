<Img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Banner_para_README5.png" >

<div>
<h2>Tabela de Conteúdo</h2> 
  <a href="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/README.md#introdu%C3%A7%C3%A3o">Introdução</a> <br>
  <a href="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/README.md#objetivo">Objetivo</a> <br>
  <a  href="#análise-descritiva-geral">Análise descritiva geral<br>
  <ul style="list-style:none; margin-left: -15px;">
    <a  href="#resumo-estatístico-das-variáveis">Resumo Estatístico das variáveis</a><br>
    <a href="#análise-preço-e-quantidade">Análise Preço e Quantidade</a><br>
    <a href="#análise-índia">Análise Índia</a><br>
    <a href="#classificação-média-dos-restaurantes">Rating : Classificação média dos restaurantes</a><br>
    <a href="#análise-do-perfil-dos-clientes">Análise do Perfil dos clientes</a><br>
    <a href="#análise-dias-na-semana">Análise Dias na Semana</a><br>
  </ul>  
 <a href="#regra-de-associcao">Regra de Associação</a><br>
 <a href="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/README.md#conclus%C3%B5es-e-insights">Conclusões e Insights</a> <br>   
 <a href="#referências">Referências</a><br>


# Introdução
<div style="text-align: justify;">
A análise descritiva será divida em duas partes: <b>Análise descritiva geral</b> e <b>Regra de Associação</b>.
<br><br>
A <b>Análise descritiva geral</b> será dividida em 6 tópicos: <b>Resumo Estatístico das variáveis, Análise Preço e Quantidade, Análise Índia, Rating, Análise do Perfil dos clientes e Análise dos dias da semana.</b>
<ul>
<li><b>Resumo Estatístico das variáveis:</b> calculo de medidas estatísticas como a média. O objetivo é entender a distribuição dos dados. Além disso, também será calculado a frequência dos valores únicos.</li>
<li><b>Análise Preço e Quantidade:</b> o objetivo é investigar as colunas relacionadas a preço e quantidade, por exemplo, preço do item e quantidade vendida.</li>
<li><b>Análise Índia:</b> analisar como dados geoeconômicos da Índia podem ser relacionar com as variáveis da tabela.</li>
<li><b>Rating:</b> descobrir mais sobre como a classificação média dos restaurantes e o número de avaliações se relacionam com as outras colunas da tabela.</li>
<li><b>Análise do Perfil dos clientes:</b> entender como informações do cliente pode estar associada ao seu comportamento de compra.</li>
<li><b>Análise dos dias da semana:</b> separar as vendas por dia da semana.</li>
</ul>

Na <b> segunda parte será feita a Regra de associação</b> usando dois algoritmos: Apriori e FP-Growth.Em seguida, será feita a análise das regras geradas, além da <b>associação de todas as regras geradas ao user_id.</b>
</div>

# Objetivo
O **objetivo inicial** era criar um **Sistema de Recomendação de categorias de comida**. Porém, durante a Análise Exploratória, descobrimos que **96% dos clientes** compram o mesmo tipo de comida.
<br>
Então, **o novo objetivo** é fazer uma **Análise Exploratória dos dados** e criar **Regras de Associação dos itens**.
<br>
Isto será feito para: 
  * Identificar padrões de compra nos pedidos. <br>
  * Obter insights sobre o comportamento dos clientes. <br>



# Análise Descritiva Geral
## Resumo Estatístico das variáveis

### **1. Resumo Tamanho da Família** 
O mínimo é 1 e o máximo é 6. A média é 3,2 e o valor 3 é o que mais aparece. 
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.1_Tabela.png" width="90%">
<br>

### **2.Resumo Valor Total do Pedido (em USD)** 
A média é 39.75 e a mediana é 15.
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.2_Tabela.png" width="50%">
<br>

### **3.Resumo Quantidade de itens encomendados**
A média é 5.36 e a mediana é 2. E, 45% das pessoas compram 1 item.
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.3_Tabela.png" width="50%">
<br>

### **4.Resumo de city**
Existem 58 valores para cidades. Porém 3 cidades estão separadas em bairros. Então o número de cidades em absoluto é um pouco menor, 44. 
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.4_Tabela.png" width="80%">
<br>

### **5.Resumo Classificação média do restaurante**
As avaliações vão de 0 à 5, sendo 0 a pontuação de restaurantes que não foram avaliados. Na limpeza dos dados foram retirados os restaurantes sem avaliação.
<br>
Após isso, o valor mínimo de avalição é 1.3 e o máximo é 5. A média é 3.8 e a mediana é 3.9.
<br> 
A proporção de notas está bem distribuída. Sendo 4 a nota com maior frequência.
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.5_Tabela.png" width="100%">
<br>

### **6.Resumo Custo médio por pessoa para uma refeição no restaurante**
A média é de 3.7 , a mediana é de 3.6 e o máximo é de 21.6. Estes valores são mais baixos que os preços de cada item. Além disso, 22% dos restaurantes tem o custo médio por pessoa de 2.4 Dóllares.
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.6_Tabela.png" width= "95%">
<br>

### **7.Resumo Tipo de cozinha oferecida pelo restaurante** 
Existem 603 tipos de restaurante, porém alguns estão combinados. Se fosse retirado o nome depois da vírgula, quantidade de tipos de restaurante cairia para 70. 
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.7_Tabela.png" width="100%">
<br>

### **8.Resumo ocupação do usuário**
Existem apenas 4 tipos de ocupação estudante (52%), empregado (31%), autônomo (13%) e dona de casa (2%).
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.8_Tabela.png" width="75%">
<br>

### **9.Resumo Renda mensal do usuário**
A maior parte dos clientes não possuem renda (47%), provavelmente, são os mesmos clientes que estudam.
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.9_Tabela.png" width="75%">
<br>

### **10.Resumo Escolaridade do usuário** 
A maior parte dos clientes tem graduação (46 %) ou Pós graduação (43%).
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.10_Tabela.png " width="75%">
<br>

### **11.Resumo Idade**
Os clientes tem uma faixa etária de 18 e 33 anos. Sendo que na média, eles tem 24 anos. 
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.11_Tabela.png" width="50%">
<br>

## Análise Preço e Quantidade
Nesta secção será analisada as colunas:
<ul>
    <li><b>veg_ou_non_veg:</B> uma classificação binária de se o alimento é vegetariano ou não vegetariano</li>
    <li><b>price_usd:</b>preço do item em Dóllar </li>
    <li><b>cost_usd:</b>estimativa do custo médio por pessoa para uma refeição no restaurante, em Dóllar</li>
    <li><b>sales_amount_usd:</b>valor total do pedido, em Dóllar</li>
    <li><b>sales_qty:</b> quantidade de itens encomendados</li>
</ul>
Também será analisada o número de pedidos.Porém, não existe uma coluna com esta informação. Então, será considerado que cada linha é um pedido.

### **12.Qual a porcentagem de alimentos vegetarianos e não vegetarinos?**
66.47 % dos alimentos são vegetarianos e 33.53% são não vegetarianos
<br> <br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.12_Grafico.png" width="100%">
<br>

###  **13.Qual a Distribuição de preço de alimentos vegetarinos?**
A média de preço é de 2.3 Dólares
<br> 
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.13_Tabela.png" width="50%">
<br>

### **14.Qual a Distribuição de preço de alimentos NÃO vegetarinos?**
A média de preço é de 3.09 Dólares
<br> 
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.14_Tabela.png " width="50%">
<br>

### **15. Ranking das 10 categorias de restaurantes com maior nº de pedidos** 
<div align="justify">
As categorias de restaurante com mais pedidos são: North Indian, Indian, Chinese, South Indian, Pizzas, Biryani, Beverages, Bakery, Desserts e Fast Food.
<br><br>
É interessante notar que as categorias em 1ª, 2ª e 4ª lugar são de comidas típicas da Índia.
<br>
Em 3ª lugar tem a comida chinesa. Provavelmente, ela é tão popular devido a sua proximidade geográfica com a Índia. 
<br>
O 6 ª lugar é ocupado pela categoria Biryani. Este tipo de comida é típico da Índia e do Paquistão. É uma comida preparada no Ramadã e em outras celebrações.
<br>
As 5ª, 7ª, 8ª, 9ª e 10ª posições são ocupadas por comidas tipicamente ocidentais.
<br><br>
OBS: Ramadã é um feriado Islâmico em que os mulçumanos realizam um jejum que se estende do nascer ao pôr do Sol. À noite, eles realizam uma refeição e um dos pratos típicos é o Biryani.
</div>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.15_Grafico.png" width="100%">
<br><br>

### **16. Ranking das 10 categorias de restaurante com os maiores preços** 
<div align="justify">
As categorias de restaurante com os maiores preços são: Japanese , Naga, Korean , Sushi e Chettinad.
<br><br>
A 1ª, 3ª e 4ª categorias mais caras são de comidas orientais.
<br>
Naga ocupa o 3º lugar como categoria mais cara. Esta cozinha é típica do Noroeste da Índia, sendo composta de arroz, carne e vegetais cozidos.
<br>
Em 4º lugar está Chettinad que é uma comida indiana do estado de Tamil Nadu (Sul da Índia). Ela é composta por uma variedade de pratos como frutos do mar como peixes, caranguejos, lagostas e camarões.
<br><br>
Algo que elas têm em comum é possuírem itens não vegetarianos. E, conforme visto no tópico Resumo Estatístico, alimentos não vegetarianos são mais caros. 
<br>
Além disso, com exceção de Naga, as outras cozinhas têm opções de frutos do mar. Talvez, essas categorias sejam caras pois a pesca na Índia seja difícil ou cara. 
</div>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.16_Grafico.png" width="100%" >
<br><br>



###  **17. Qual o custo médio por pessoa nos restaurantes das 10 cidades com mais pedidos?**
<div align="justify">
No resultado final, as cidades de Bangalore e Ahmedabad estão separadas por distritos. Por exemplo, JP Nagar, Bangalore significa o distrito JP Nagar na cidade de Bangalore. A mesma lógica pode ser aplicada para os outros resultados.
<br><br>
A divisão por distritos nestas duas cidades talvez possa ser explicado pois elas são grandes centros econômicos da Índia. 
<br><br>
Os maiores custos ficam nas cidades do sul e sudoeste. Bangalore é a cidade com o maior custo médio, seguida por Ahmedabad.
<br><br> 
As cidades Allahabad, Amritsar e Aurangabad ocupam os 3º, 4º e 5º lugar respectivamente e tem custos médios muito parecidos. 
</div>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.17_Grafico.png" width="100%" >
<br><br>

**Mapa**
<br>
O mapa a seguir foi feito no Power Bi
<br>
<center>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.17_mapa_custo_medio_por_pessoa_nos_restaurantes_das_cidades_com_mais_n%C2%BA_pedidos.png" with="70%">
</center>

### **18. Quais as cidades com os mais pedidos?**
<div align="justify">
No resultado final, as cidades de Bangalore e Ahmedabad estão separadas por distritos. Por exemplo, JP Nagar, Bangalore significa o distrito JP Nagar na cidade de Bangalore. A mesma lógica pode ser aplicada para os outros resultados.
<br>
A divisão por distritos nestas duas cidades talvez possa ser explicada pois elas são grandes centros econômicos da Índia.
<br><br>
Bangalore e Ahmedabad são as cidades com mais pedidos. Elas se localizam respectivamente, no sul e sudeste da Índia. 
<br>
As cidades Adityapur, Amritsar, Allahabad e Aurangabad ocupam os 3º, 4º, 5º e 6º lugar.
</div>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.18_Grafico.png" width="100%" >
<br><br>
Foi feito no Power Bi um mapa das cidades com mais vendas
<center>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.18_mapa_cidades_com_mais_n%C2%BA_pedidos.png" width="100%" >
<br><br>

</center>

### **19. Ranking das 10 categorias de restaurante com menores preços (custo médio por refeição)** 
**OBS:** Os preços são calculados em Dóllar Americano
<br><br>
As categorias com o menor custo médio por refeição são Italian-American ,  Rajasthani , Juices e Café.
Rajasthani é uma culinária do noroeste da Índia.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.19_Grafico.png" width="100%" >
<br><br>

### **20. Quais as cidades com o custo médio de refeição por pessoa mais caro?** 
As cidades de Bangalore e Ahmedabad possuem o custo por refeição mais caro. Elas também são as cidades com os maiores números de pedidos.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.20_Grafico.png" width="100%" >
<br><br>
<center>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.20_card_cidades_custo_mais_caro.png" width="100%">
</center>

### **21. Quais as cidades com o custo médio de refeição por pessoa mais barato?** 
As cidades do nordeste são as que tem o custo por refeição mais barato. Seguidas de algumas cidades ao sul.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.21_Grafico.png" width="100%" >
<br><br>

O mapa a seguir foi feito no Power Bi
<br>
<center>
<img src= "https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.21_mapa_cidades_com_custo_medio_de_refeicoes_por_pessoa_maiores_barato.png" width="100%" >
</center>
<br><br>

### **22. Cidades com os maiores valores totais por pedido (sales_amount)**
Ahmedabad, Agra, Adoni, Abohar, Allahabad, Alligarh, Agartala e Alappuzha são as cidades que possuem maiores valores totais por pedido.
<br><br>
Ahmedabad está sudoeste e as outras cidades estão no norte da Índia, com exceção de Adoni que está no sul. <br>
As cidades Ahmedabad, Agra e Allahabad são grandes centros econômicos. Em Agra fica localizado o Taj Mahal.<br>
Já Adoni, Abohar, Alligarh e Agartala são centros regionais importantes em seus respectivos estados. <br>
E, Alappuzha é um importante centro turístico. A cidade é conhecida pelos seus canais e backwaters.
<br>
Fontes: <a href="https://pt.wikipedia.org/wiki/Economia_da_%C3%8Dndia">Wikipedia</a> e <a href="https://www.investindia.gov.in/pt-br/great-places-for-manufacturing-in-india">Investindia.gov.in</a>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.22_Grafico.png" width="100%" >
<br><br>

O mapa a seguir foi feito no Power Bi
<br>
<center>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.22_mapa_cidades_com_maiores_valores_totais_por_pedido_(sales_amount)1.png" width="100%" >
</center>
<br><br>

###  **23. Tipos de restaurantes com os maiores valores totais por pedido (sales_amount)** 
Os tipos de restaurante com maior sales_amunt são: Mexican, Asian, Grill, Gujarati, Costal, French, Combo, Continental, Hyderabadi e Bengali.
<br><br>
Gujarati é uma comida do estado de Gujarat na Índia. Ela é principalmente vegetariana. E, tem como ingredientes uma variedade de grãos, lentilhas e vegetais.
<br><br>
A culinária Costal é típica da região costeira da Índia e usa como ingrediente frutos do mar frescos, ervas aromáticas e uma variedade de temperos.
<br><br>
Continental é um termo generalizado que se refere coletivamente à culinária da Europa e de outros países ocidentais. Nela, a carne é o prato principal. 
<br><br>
Hyderabadi é uma mistura da culinária Mughlai e do norte da Índia, com influência das especiarias e ervas da comida nativa Telugu. Esta comida leva temperos, carne, arroz; também faz uso de coco e tamarindo.
<br><br>
Bengali é um estilo culinário de Bengala, que compreende Bangladesh e os estados indianos de Bengala Ocidental e Tripura. Ela tem como ingredientes arroz, lentilhas, peixe, carne bovina e de cabra.   
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.23_Grafico.png" width="100%" >
<br><br>

### **24. Cidades com maiores nº de pedidos: Valores totais por pedido (sales_amount) vs nº de pedidos**
A cidade de Ahmedabad apresenta três resultados:
<ul>
<li>O distrito de Vastrapur tem um valor total por pedido alto e um número de pedidos mediano. Curiosamente, este distrito é pequeno, porém muito povoados.</li>
<li>Os distritos de Navrangpura tem um valor total por pedido e um número de pedidos baixos. Ele também é um distrito pequeno e muito povoado.</li> 
<li>O distrito Gandhinagar têm um valor total de pedidos mediano e um número de pedidos baixo. Ele é um distrito grande. Porém, é pouco povoado.</li> 
</ul>

A cidade de Bangalore também apresenta dois resultados contrastantes:
<ul>
<li>O distrito de JP Nagar tem números de pedidos mediano e valor total de pedido baixo. Ele tem um tamanho moderado. Entretanto, é muito povoado.</li>
<li>Os distritos de Koramangala e HSR, tem um alto número de pedidos, porém com baixo valor total. Eles são distritos pequenos, porém muito povoados.</li>
</ul> 

<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.24_card_city3.png" width="80%">
<br>
Fonte:<a href="https://geoiq.io/places/Koramangala/6P0l0H8Jya">geoIQ</a>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.24_Grafico.png" width="100%" >
<br><br>

## Análise Índia
O objetivo desta parte é analisar algumas informações geoecônomicas da Índia e relacioná-las com as variáveis desta base de dados.

Segundo o site [StatisticsTimes.com (2021)](https://statisticstimes.com/demographics/country/india-cities-population.php), as 10 cidades mais populosas da Índia são: <br>
**1º Délhi (Delhi)** <br>
**2º Mumbai (Bombaim)** <br>
**3º Calcutá (Calcutá)** <br>
**4º Bangalore**<br>
**5º Chennai (Madras)** <br>
**6º Hyderabad** <br>
**7º Ahmedabad** <br>
**8º Carta** <br>
**9º Puna (Pune)** <br>
**10º Jaipur**

De acordo com o site [Statista (2022)](https://www.statista.com/statistics/1400141/india-gdp-of-major-cities/#:~:text=GDP%20share%20of%20cities%20in%20India%202022&text=In%20the%20year%202022%2C%20Mumbai,six%20megacities%20topped%20the%20list.), as cidades que mais contribuem para o PIB da Índia em 2022 são:<br>
**1º Mumbai:** 310 Bilhões de Dóllares americanos<br>
**2º Delhi:** 293.6 Bilhões de Dóllares americanos<br>
**3º Kolkata:** 150 Bilhões de Dóllares americanos <br>
**4º Bangalore:** 110 Bilhões de Dóllares americanos <br>
**5º Chennai:** 78.6 Bilhões de Dóllares americanos <br>
**6º Hyderabad:** 75 Bilhões de Dóllares americanos <br>
**7º Pune:** 69 Bilhões de Dóllares americanos <br>
**8º Ahmedabad:** 68 Bilhões de Dóllares americanos <br>
**9º Surat:** 59.8 Bilhões de Dóllares americanos <br>
**10º Vishakhapatnam:** 48.5 Bilhões de Dóllares americanos <br>

<mark><b>Apenas as cidades de Bangalore e Ahmedabad estão nas listas acima e também na base de dados.</b></mark>
<br><br>
<mark><b>Não foi encontrado o PIB per capita das cidades da base de dados.Entretanto, foi encontrado o número de residentes em favela.Este valor será utilizado como uma espécie de proxy.</b></mark>
<br><br>
Por isso, será analisada a **população**, **religião** e o **número de moradoes em favelas** de cada cidade da base de dados.E para descobrir estas informações foi criada no Excel uma tabela com dados retirados do site [Census 2011 Índia (2011)](https://www.census2011.co.in/). 
 
A hipótese usada na coluna **número de moradores** em favelas é a seguinte:
<ul>
Supõe-se que pessoas que moram em favela tenham um poder aquisitivo mais baixo. Por isso, terão menos dinheiro para comer fora e comprar lanche aplicativos como Zomato. <br>
Então, espera-se que haja alguma associação entre a porcentagem de moradores em favela e um baixo número de pedidos e preços.<br>
Vale ressaltar que o objetivo é verificar se existe associação entre as variáveis, mesmo que não seja possível identificar uma causalidade.   

</ul>
Para verificar se esta lógica está correta, será testada a correlação da porcentagem de moradores em favela com as variáveis relacionadas a preço e quantidade (nº de pedidos).
<br><br>
A seguir, a Tabela com as informações geoeconômicas da Índia retiradas do site <a href="https://www.census2011.co.in/ ">Census 2011 Índia (2011)</a>.Vale Ressaltar que em algumas cidades não foi encontrada o número de moradores em favela.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Tabela_An%C3%A1lise_%C3%8Dndia_infoma%C3%A7%C3%B5es_geoecon%C3%B4micas.png" width="95%" >
<br><br>

###  **25. Relação entre o preço por item e porcentagem de residentes que moram em favela** 
Em ambas as correlações, o p-valor foi baixo. Portanto a associação entre as variáveis é significativa. Já os coeficientes foram positivos e baixos.
<br><br>
Isso indica que existe associação entre o preço por item e a porcentagem de residentes que moram em favelas. Esta associação é positiva e fraca.
<br><br>
Portanto, cidades com altos preços por item, também possuem alto número de favelas. Este resultado pode indicar que as cidades indianas tem grande desigualdade econômica e também explica o porque de 45% das pessoas desta base de dados comprarem apenas 1 item (visto na pergunta 3)
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.25_Correlacoes.png" width="80%" >
<br><br>

### **26. Relação entre custo médio da refeição e porcentagem de residentes que moram em favela** 
Em ambas as correlações, o p-valor foi muito baixo e a correlação fraca. A Correlação de Pearson resultou em um valor positivo, enquanto a Correlação de Spearman foi negativa.
<br>
Portanto, há envidência <mark>**de uma relação entre o custo médio por refeição por cidade e a porcentagem de moradores de favela por cidade. Porém, a forma desta relação não é clara.**</mark>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.26_Correlacoes.png" width="80%" >
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.26_Grafico.png" width="100%" >
<br><br>

### **27. Relação entre a porcentagem de residentes que moram em favela e a média do valor total de pedidos (sales_amount_usd)** 
O p-valor das duas correlações foi significativo.
E, ambos os coeficientes indicam que há uma relação negativa entre valor total do pedido e nº de moradores de favela, de modo que quando uma variável aumenta.
<br><br>
De modo geral, pode-se dizer que <mark>**há associação negativa entre o valor total do pedido e nº de moradores de favela.**</mark>. De modo que quando uma variável aumenta, a outra diminui.De modo que quando uma variável aumenta, a outra diminui. <br><br>
Este resultado faz sentido, pois um grande número de moradores em favela pode ser um indicativo de pobreza, logo, as pessoas não tem muito dinheiro disponível para gastar com lanche.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.27_Correlacoes.png" width="80%" >
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.27_Grafico.png" width="100%" >
<br><br>

###  **28. Quais as 15 cidades com os maiores pedidos por habitante?** 
Para responder esta pergunta será feita a contagem do número de pedidos por cidade. Em seguida, será carregada a tabela com a população por cidade. E depois , será feita a união das duas tabelas. 
<br><br>
Então, será feito o cálculo a seguir:
<br><br>
<center>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.28_numero_de_pedidos_por_habitante1.png" width="80%">
</center>
<br><br>
As cidades com os maiores pedidos por habitante são: Balrampur, Agartala, Adityapur, Bagdogra, Baddi e Bahadurgarh.
<br>
Estas cidades tem algo em comum: são de tamanho médio e com rápido crescimento econômico. 
<ul>
    <li>Balrampur é um centro industrial e comercial. Ela abriga a Chini Mills, uma das maiores usinas de açúcar da Índia e tem cerca de 200.000 habitantes.</li>
    <li>Agartala abriga várias universidades e instituições de pesquisa. Ela possui cerca de 500.000 habitantes.</li>
    <li>Adityapur possui várias empresas de grande porte, incluindo a Tata Steel. E, sua população é de cerca de 200.000 habitantes.</li>
    <li>Em Bagdogra há um importante aeroporto internacional. A cidade possui cerca de 100.000 habitantes.</li>
    <li>Baddi abriga várias empresas farmacêuticas e de manufatura. Sua população é de cerca de 50.000 habitantes.</li>
    <li>A cidade Bahadurgarh tem várias empresas de grande porte, como a Suzuki. Sua população é de 200.000 habitantes.</li>
</ul>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.28_Grafico.png" width="97%" >
<br><br>

###  **29. Qual a correlação entre o número de pedidos por cidade e o tamanho da população?**
Existe uma correlação positiva e <b>forte</b> entre tamanho da população e número de pedidos. Além disso, o p-valor é  muito pequeno, logo, está associação linear é estatisticamente significativa.
<br><br>
Em geral,  <mark>**há uma associação entre número de pedidos e tamanho da população.**</mark> 
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.29_Correlacao.png" width="80%" >
<br><br>

### **30. Distribuição da Religião Predonominante nas cidades da base de dados. E o tipo de comida com mais pedidos em cada cidade.** 
O mapa a seguir foi feito no Power Bi usando Tabela <code>nome_city5</code> criada no início da secção <code> Análise Índia</code>
<br>
É possível observar no mapa que a religião Predominante é o Hinduísmo, seguido do Islamismo. Isso é importante, pois <mark>**a religião pode influenciar os hábitos alimentares, por exemplo, com restrição a algum alimento.**</mark>
<br>
Além disso, <mark>**cada religião tem suas datas festivas que podem influenciar as vendas neste período.**</mark>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.31_Painel%20(3500%20x%204000%20px).png" width="100%">

###  **31. Qual a Relação entre Religião Predominante e Tipo de cozinha com maior número de pedidos?** 
**Processo:**
<br>
OBS: A religião predominante está por cidade. 
<br>
Nesta base de dados, as cidades cuja religião predominante é:
<ul>
<li><b>Hinduísmo</b> compram mais <b>North indian</b>, <b>Indian</b>, <b>Chinese</b> e <b>South indian</b></li>
<li><b>1.Hinduismos_2.Islamismos:</b>Quando a religião com mais fiéis é Hinduísmo e a segunda é Islamismo, as pessoas compram mais comida <b>North indian</b>, <b>Chinese</b>, <b>Indian</b> e <b>Pizzas</b> .</li>
<li><b>1.Islamismo_2.Hinduísmo: </b> Quando a religião com mais fiéis é Islamismo e a segunda é Hinduísmo, as pessoas compram mais comida <b>North indian</b>, <b>Pizzas</b>,<b> Chinese</b>, <b>Italian</b></li>
<li><b>Hinduísmo</b> e <b> Cristianismo</b> compram mais comida <b>South indian</b>, <b>Kerala</b>, <b>North indian </b> e <b>Continental</b>.</li>

<li><b>Hinduísmo</b> e <b>Sikhismo</b> compram mais comida <b>North indian</b>, <b>Pizzas</b>,<b>American</b> e <b>Fast Food</b>.</li>
</ul>
Pode-se concluir que a religião predominante de uma cidade influência nos gostos culinários dos clientes daquela localização. 
#### **Painel**
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.30_mapa_distrib_religiao_por_cidade2.png" width="100%" >
<br><br>

## **Classificação média dos restaurantes**
### **32. Existe alguma correlação entre a classificação média do restaurante e o número de avaliações?** 
A correlação de Pearson foi de 0.14 e o p-valor foi muito baixo. Indicando que há uma associação linear entre as duas variáveis, porém esta associação é fraca.
<br><br>
Já a correlação de Pearson foi de 0.21 e o p-valor também foi muito baixo. O indicando que há uma associação positiva e moderada entre as variáveis.
<br><br>
Pode-se concluir que <b>há associação entre as variáveis</b>. De modo que,  quando a classificação média do restaurante, o número de avaliações também aumenta. Entretanto, esta associação não implica em causalidade, é possível que outros fatores influenciem esta relação.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.32_Correlacoes.png" width="80%" >
<br><br>

### **33. Existe correlação entre a classificação do restaurante e o custo médio por pessoa?** 
Em ambas as correlações o resultado foi positivo e o p-valor foi muito baixo. Indicando que existe associação entre associação entre as variáveis. De modo, que um aumento da classificação do restaurante está associado a um aumento no custo médio. 
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.33_Correlacoes.png" width="80%" >
<br><br>

### **34. Qual a correlação entre o preço médio da refeição e a classificação do restaurante?** 
As correlações deram um valor positivo e baixo. E, os p-valor foram significativos. Portanto, existe uma associação positiva (mas fraca) entre o preço médio da refeição e a classificação do restaurante.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.34_Correlacoes.png" width="80%" >
<br><br>

###  **35. Quais os tipos de restaurantes com a pontuação mais alta?**
As comidas Paan , Ice Cream, Waffle e Coastal possuem  as pontuações mais altas.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.35_Tabela.png" width="50%" >
<br><br>

###  **36. Qual a classificação média das 10 categorias de restaurantes com preço médio mais alto?** 
Foi analisado os 10 tipos de restaurantes com maiores os preços mais altos. A partir daí, foi encontrado a classificação média deles.
<br>
Não há uma relação clara entre as duas variáveis. Por exemplo, Japonese é o tipo de restaurante com o maior preço e também possui uma classificação alta. Entretanto, Middle Eastern tem um dos preços mais baixos e também possui uma classificação alta.
<br>
<mark>**Pode-se afirmar que os tipos de restaurantes com maiores preços têm boas classificações (acima de 3.8)**</mark> 
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.36_tabela_preco_e_classificacao1.png" width="90%">
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.36_Grafico.png" width="100%" >
<br><br>

## Análise do Perfil dos clientes
### **37. Qual o Tamanho médio  das Famílias ?** 
O tamanho médio das famílias é de 3 à 4 pessoas. 
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.37_card_tamanho_familia.png" width="55%" >
<br><br>


###  **38. Qual a porcentagem de mulheres e homens ?** 
Há 43% de clientes mulheres e 56% de clientes homens
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.38_Grafico.png" width="80%" >
<br><br>

### **39. Valor total do pedido (sales_amount_usd) x  Tamanho das Famílias** 
Foi utilizado a média e a mediana do valor total do pedido. Pois estes dois valores são bem diferentes.
<ul>
   <li><b>Usando a Média:</b>As famílias tem de 1 à 6 membros. E, as famílias com 5 pessoas são as que mais gastam ; seguidas das famílias com 1 e 6 pessoas. As famílias com 2 e 4 membros têm os menores gastos.</li>
   <li><b>Usando a Mediana:</b> As famílias com 6 membros tiveram o maior gasto, seguido pelas famílias de 5,4 e 3 membros.</li>
</ul>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.39_Tabela.png" width="50%" >
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.39_Grafico_Media.png" width="95%" >
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.39_Grafico_Mediana.png" width="95%" >
<br><br>


### **40. Preço do item comprado (price_usd) x  Tamanho das Famílias** 
Será analisada a relação entre o preço dos itens comprados e o tamanho da família. Para isso será utilizado a média e a mediana de ‘price_usd’.
<br><br>
A média tem valores mais altos do que a mediana. E, a diferença entre as duas é baixa.
<ul>
  <li><b>Usando a Média:</b>os valores são bem próximos. As famílias com 2 membros compram itens mais caros. Em seguida, estão as famílias com 1, 5, 4, 3 e 6 membros.</li> 
  <li><b>Usando a Mediana:</b> Os valores são bem parecidos. Famílias de tamanho 1, 2 e 4 compram a mesma quantidade de itens. Da mesma forma, famílias com 3,5 e 6 pessoas também compram a mesma quantidade de itens.</li>
</ul>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.40_Tabela.png" width="90%" >
<br><br>

### **41. Quantidade de itens comprados (sales_qty) x  Tamanho das Famílias** 
Será analisada a relação entre a quantidade de itens comprados e o tamanho da família. Para isso será utilizado a média e a mediana de ‘sales_qty’.
<br><br>
A média tem valores mais altos do que a mediana. E, a diferença entre as duas é grande.
<ul>
  <li><b>Usando a Média:</b> famílias de tamanho 4 compram a maior quantidade de itens. Seguidas pelas famílias de tamanho 3,5,6 e 1, respectivamente.</li> 
  <li><b>Usando a Mediana:</b> os valores são iguais, todas compram 2 itens.</li>
</ul>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.41_Tabela.png" width="90%" >
<br><br>


### **42. Valor total do pedido (sales_amount) X  renda mensal do usuário (Monthly Income)**
O objetivo agora é analisar a relação entre o valor do pedido total e a renda mensal do cliente. Na documentação da base de dados não foi especificada em que moeda está a renda mensal. 
<br>
Ela está dividida em 5 categorias:
<ul> 
  <li>Sem renda;</li> 
  <li>Renda menor que 10.000;</li>
  <li> Entre 10.001 e 25.000;</li>
  <li> Entre 25.001 e 50.000; </li>
  <li>Mais que 50.000 . </li> 
</ul>
<br>
Além disso, como a média e mediana do valor total do pedido são diferentes, será analisado ambos.
<ul> 
  <li>
  <b>Usando a Média:</b> parece não haver um padrão entre o valor da renda e o valor do pedido. Pessoas que ganham <b>entre 25.001 e 50.000</b> são as que tem <b>maior valor total do pedido.</b> <br>
  Em <b>segundo lugar</b> estão as <b>pessoas sem renda (no income)</b>. <br>
  Em <b>terceiro lugar</b> estão as pessoas que ganham <b>entre 10.001 e 25.000</b>. Estas duas categorias têm valores muito próximos, com diferença de 0.16 USD. <br>
  E, <b>por último</b>, estão as pessoas que ganham <b>menos que 10.000</b>.
  </li>
  <li>
  <b>Usando a Mediana:</b> também parece não haver um padrão entre as variáveis.Porém, os valores são muito parecidos. <br>
  As pessoas que ganham entre <b>10.001 e 25.000</b> tem <b>os maiores valores do pedido total.</b> 
  Em <b>segundo lugar</b> está as pessoas <b>sem renda (no income).</b> <br>
  E, em <b>terceiro e quarto lugar</b> estão, respectivamente, as pessoas que ganham  <b>More than 50.000</b> e <b>25.001 to 50.000</b>. A diferença entre as duas posições é baixa, de 0,05 USD. <br>
  Em <b>último lugar</b> estão as pessoas que ganham <b>menos que 10.000</b>.
 </li>
</ul>
<br>
Levando em considerando os resultados usando a média e a mediana. Pode-se concluir algumas coisas:
<ul style="list-style: circle;">
  <li>Em geral, pessoas que ganham menos que 10.000 são as que gastam menos por pedido na Zomato. 
  </li>
  <li>Pessoas sem renda têm os maiores valores totais por pedido. Algo que pode ser contraditório. Porém, levando em consideração que os clientes tem entre 18 e 33 anos, é possível que essas pessoas sem renda sejam estudantes bancados pelos pais que possuem um bom poder aquisitivo.
  </li>
  <li>Pessoas que ganham entre 25.001 e 50.000 também gastam por pedido muito na Zomato.</li>
</ul>
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.42_tabela_valor_do_pedido_e_renda_mensal2.png" width="100%" >
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.42_grafico.png" width="100%" >
<br><br>

## **Análise Dias na Semana**
### **43. Geral: Número de Vendas por Dia da Semana** 
Será feita a contagem das vendas feitas em cada dia da semana de forma geral (usando todos os anos disponíveis na base).
<br><br>
Sobre o resultado, o que mais chama a atenção é que nos fins de semana o número de vendas cai bastante. Foi pesquisado o motivo disso acontecer, porém não foi encontrado uma explicação.
<br>
Algumas teorias podem explicar isso:
<ul style="list-style: decimal;">
  <li>
    Pode ser que o sistema da Zomato não registre as vendas nos fins de semana, deixando para fazer isso na segunda, por exemplo.
  </li>
  <li>
    Também é possível que os indianos prefiram cozinhar em casa nos fins de semana. Não foi encontrado nenhum artigo que trate do assunto, porém há uma postagem do site Quora explicando que é uma norma cultural as famílias indianas compartilharem refeições e que “cozinhar em casa é muitas vezes a principal forma de fornecer refeições.” <a href="https://www.quora.com/Do-Indians-order-less-food-when-eating-out-but-cook-more-at-home">(MONDOL,T; 2023)</a>
  </li>
  <li>
    Uma terceira teoria é que nos fins de semana, os indianos preferem comer fora. De acordo com um estudo feito por
    <a href="https://ieeexplore.ieee.org/abstract/document/7754477">Mohan et. al (2016)</a>, as famílias indianas tem mudado seus hábitos e passam os fins de semana em complexos comerciais, como shoppings. Devido a isso, as famílias têm feito as refeições dos fins de semana nas praças de alimentação ou em restaurantes próximos aos shoppings.
  </li>
</ul>
<br>
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.43_Grafico.png" width="90%" >
<br><br>

### **44. Vendas por Dia da Semana para Cada Ano** 
Buscou-se analisar vendas em cada dia semana separadas pelos anos.
<br>
É possível observar que em 2018 e 2019 houve um aumento nas vendas. Porém em 2020 , as vendas diminuíram, provavelmente, isso aconteceu por causa da pandemia de Covid19. 
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.44_Tabela.png" width="50%" >
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.44_Grafico.png" width="90%" >
<br><br>

# Regra de associação 
## Introdução à Regras de Associação
As regras de associação ajudam a descobrir relacionamentos entre itens de uma base de dados. Essas regras possuem alguns elementos importantes como:<br>
**Antecedentes**: Conjunto de itens que precisam estar presentes na transação para que a regra se aplique.<br>
**Consequentes**: Conjunto de itens que é previsto pela regra. Em outras palavras, se uma transação contém o(s) antecedente(s), a regra prevê que ela também conterá o(s) consequente(s) com uma certa probabilidade.
Supondo que o antecedente seja leite o consequente seja pão.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Regra_de_Associa%C3%A7%C3%A3o/leite.implica.em.pao.png" width="50%" >
<br><br>

**Antecedent support:** Proporção de transações no seu conjunto de dados que contém o(s) antecedente(s). 
<br>
Por exemplo, supondo que antecedent support é igual a 0.14. Significa que 14% das transações da base de dados possuem leite.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Regra_de_Associa%C3%A7%C3%A3o/antecedent_support.png" width="70%">
<br><br>


**Consequent support:** Proporção de transações no seu conjunto de dados que contém o(s) consequente(s).
<br>
Por exemplo, supondo que consequent support é igual a 0.21. Significa que 21% das transações da base de dados possuem pão.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Regra_de_Associa%C3%A7%C3%A3o/consequent_support1.png" width="70%">
<br><br>

**Support:** Proporção de transações no seu conjunto de dados que contêm ambos os itens, tanto o antecedente quanto o consequente. Ou seja, é o número de transações para as quais uma regra faz a predição correta (utilidade). Suporte está associado a significância de estatística da regra.
<br>
Esta métrica serve para eliminar regras pouco interessantes, ou, eliminar conjunto de itens que não atendem ao critério mínimo.
<br>
Por exemplo, sendo o antecedente pão e o consequente leite. Se o support for igual a 0.10, significa que 10% das transações contém pão e leite juntos.
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Regra_de_Associa%C3%A7%C3%A3o/support.png" width="70%">
<br><br>

**Confidence:** número de transações que a regra prediz corretamente entre as transações para as quais a regra se aplica (certeza). Ou seja, esta medida define a probabilidade de ocorrência do consequente no carrinho dado que o carrinho já possui os antecedentes. Esta métrica está associada a acurácia ou precisão.
<br>
Por exemplo, se o confidence for igual a 0.76, significa que há 76% de chance de uma transação que tem pão também ter leite.
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Regra_de_Associa%C3%A7%C3%A3o/confidence.png" width="70%">
<br><br>

**Lift:** mede o grau em que dois itens são dependentes um do outro, em comparação com o que seria esperado se fossem independentes. 
<br>
Um valor de elevação de 1 indica que os dois itens são independentes, um valor maior que 1 indica uma associação positiva, enquanto um valor menor que 1 indica uma associação negativa.
<br>
Por exemplo, se lift for igual a 2.1 , significa que a chance de encontrar pão e leite juntos é 2.1 vezes maior do que encontrar cada um individualmente.

## Interpretação do Resultado da Regra de Associação 2 
### Algoritmo Apriori
Com base nos parâmetros escolhidos, foram encontradas 36 regras únicas usando o algoritmo Apriori. Nota-se que há um padrão, com valores baixos de Support e valores altos/moderados de Confidence e lift. 
<br><br>
Isso mostra que **<mark>há uma alta probabilidade de os alimentos das regras serem comprados juntos. Porém essas regras acontecem com pouca frequência.</mark>** 
<br>
Além disso, também é possível concluir que **<mark>as chances de os alimentos da regra serem comprados juntos é maior que de serem comprados separados.</mark>**
<br><br>

### **Dal Fry e Jeera Rice**
Dal Fry é um prato popular indiano feito com lentilhas, cebola, tomate, especiarias e ervas.
<br>
 Jeera Rice é um prato indiano composto por arroz e sementes de cominho. É um prato muito popular no subcontinente indiano e mais comumente usado como prato de arroz todos os dias.
 <br>
 <img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Regra_de_Associa%C3%A7%C3%A3o/card_Dal_e_Jeera.png" width="90%">
 <br>
 Na linha 118  Dal Fry foi o antecendente e o consequente foi Jeera Rice. Ou seja, a compra de Dal Fry implica na compra de Jeera Rice. 
<br>
Na linha 119, os antecendentes e consequentes desta regra mudam. Portanto, pode-se concluir que há uma associação na compra de Dal Fry e de Jeera Rice.
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Regra_de_Associa%C3%A7%C3%A3o/Tabela_Interpreta%C3%A7%C3%A3o_Regra_de_Associa%C3%A7%C3%A3o.png" width="100%">
<br><br>
Nesta base de dados, a proporção de Dal fry é de 17%, enquanto a proporção de Jerra Rice é de 25%. 
<br><br> 
O suporte da linha 118 e da linha 119 são de 0.13, ou seja, 13% das transações desta base de dados possuem Dal Fry e Jeera Rice.
<br><br>
Confidence das linhas 118 e 119 são diferentes. Esta métrica é, respectivamente, igual a 0.8 e 0.54. Portanto:
<ul>
  <li><b>Regra de Associação da linha 118:</b> Dada uma transação que há Dal Fry, há 80% de chance desta transação também conter Jeera Rice.
  </li>
  <li><b>Regra de Associação da linha 119:</b> Dada uma transação que há Jeera Rice, há 54% de chance desta transação também conter Dal Fry.
  </li>  
</ul>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Regra_de_Associa%C3%A7%C3%A3o/insight_reg_ass1.png" width="100%">
<br><br>
O **lift** das duas regras é de 3,13 Isso significa que as chances de encontrar Dal Fry e Jeera Rice juntos é 3,13 vezes maior do que encontrar cada um individualmente. Pode-se concluir estes dois itens são altamente dependentes um do outro, logo costumam ser comprados juntos.
<br>
Em suma, clientes que compram Dal Fry também compram Jeera Rice. Além disso, este tipo de análise pode ser feita da mesma forma para os outros itens.

###  **Cliente 59455**
A seguir será feita a análise das regras de associação para a cliente com **user_id 59455**. Este id foi escolhido de forma aleatória. 
<br><br>
O nome desta cliente é Joshua Jimenez, ela tem 27 anos e é pós graduada. Além disso, possui uma família com 5 membros, está empregada e tem uma renda mensal entre 25.001 e 50.000. Provavelmente, ela mora no distrito de Navrangpura, na cidade de Ahmedabad.
<br><br>
Entre os itens comprados por ela estão **Dal Fry** e **Jeera Rice**. Com base nisso, algumas recomendações para futuras compras são:
<br>

 #### <b>Recomendações para quem compra <mark>Dal Fry (Apriori)</mark></b>
 <ul>
   1. Butter Naan <br>
   2. Chana Masala <br>
   3. Chicken Fried Rice <br>
   4. Dal Makhani <br>
   5. Egg Fried Rice <br>
   6. Veg Fried Rice
</ul>
<br>

#### <b>Recomendações para quem compra <mark>Dal Fry (FP-Growth)</mark></b>
<ul>
   7. Garlic Naan <br>
   8. Gobi Manchurian <br>
   9. Egg Curry <br>
   10. Green Salad <br>
   11. Veg Noodles <br>
   12. Mushroom Chilli <br>
</ul>
<br>

#### <b>Recomendações para quem compra <mark>Jeera Rice (Apriori)</mark></b>
   <ul>
     1. French Fries <br>
     2. Plain Rice <br>
     3. Shahi Paneer <br>
     4. Tandoori Roti <br>
     5. Tomato Soup <br>
     6. Veg Pulao <br>
  </ul>
<br>

#### <b>Recomendações para quem compra <mark>Jeera Rice  (FP-Growth)</mark></b>
<ul>
  7. Chicken Tikka Masala <br>
  8. Ghee Rice <br>
  9. Kadai Paneer <br>
  10. Dal Tadka <br>
  11. Cheese Sandwich <br>
  12. Veg Schezwan Fried Rice <br>
</ul>

# Conclusões e Insights
## 1.  Os clientes são jovens (entre 18 e 33 anos)
O que pode ser feito? Atrair clientes de outras faixas etárias.
<ul>
<li>Pode ser feito uma pesquisa para entender o motivo de pessoas mais velhas não usarem o aplicativo. Algumas hipóteses são:</li>
    <ul>
        <li>A usabilidade do aplicativo não é amigável para pessoas mais velhas. Então, a solução seria mudar o layout do aplicativo.</li>
        <li>Pessoas de outras faixas etárias não conhecem o app Zomato. Se for este o caso, a empresa poderia fazer divulgação em plataformas que pessoas mais 
         velhas usam. Por exemplo, fazer anúncios no Facebook. </li>
        <li>Os alimentos disponíveis no app não agradam pessoas mais velhas. Neste caso, a Zomato poderia mapear os gostos culinários desta faixa etária e 
        tentar atrair para o app restaurantes compatíveis com tais preferências.</li>
    </ul>
</ul>
<br>

## 2. Ampliação da presença em cidades universitárias
No tópico 42, foi descoberto que pessoas sem renda tem o segundo valor total por pedido. Levando em consideração que o público da Zomato é jovem. Possivelmente, estas pessoas são universitárias bancadas pelos pais.
Esta hipótese é validada pelo tópico 22. Nele, descobriu-se as cidades que possuem os maiores valores totais por pedido. Por exemplo, 
  * Ahmedabad tem o maior valor total por pedido e ela abriga a Indian Institute of Management Ahmedabad (IIMA), uma das principais escolas de administração 
    da Índia.
  *  Allahabad tembém abriga outra universidade importante, a University of Allahabad
Portanto, uma estratégia seria ampliar a presença da Zomato em cidades com grande número de universidades.
<br>

## 3. 48% dos restaurantes não tem avaliação
Isso é um problema caso a empresa queira fazer um sistema de recomendação, por exemplo. A solução seria incentivar os clientes a avaliarem os restaurantes. Como isso pode ser feito? A empresa poderia oferecer cupons de desconto para quem avaliassem certo número de restaurantes. 
<br>

## 4. Produtos vegetarianos são os mais vendidos
Isto não é um problema. Porém quando a Zomato aceitar um restaurante em seu app, deve se atentar se ele tem opções vegetarianas no cardápio. Vale ressaltar que alimentos vegetarianos também são os mais baratos. 
<br>

## 5. As comidas mais populares variam em cada cidade
Um indicativo dos tipos de comida mais populares é a religião predominante da cidade. 
<br>
Por exemplo, cidades cuja religião predominante é puramente Hinduísmo tem preferencias diferentes de cidades cujas as religiões predominantes são em primeiro lugar Islamismo e em segundo lugar Hinduísmo (1.Islamismo_2.Hinduismo).
<br><br>
Então, se por acaso, as vendas estiverem baixas em alguma cidade, seria útil o app Zomato procurar parcerias com restaurantes que possuem as categorias de comidas preferidas da religião predominante daquela cidade.
<br><br>
Ou ainda, se a Zomato começar a operar em uma nova cidade, esta associação entre comida mais popular e religião predominante na cidade, será útil para a empresa direcionar melhor a busca por restaurantes parceiros.
<br>

## 6. Ampliar presença em grandes centros econômicos e cidades de médio porte em expansão rápida
Grandes centros econômicos como Ahmedabad possuem os maiores números de pedido e os maiores valores totais por pedido. Entretanto, na base de dados não há muitos grandes centros, como Calcultá. Logo, este é mercado pouco explorado pela Zomato.
<br><br>
Além disso, cidades de médio porte com rápido crescimento econômico, como Agartala, são as que possuem os maiores números de pedidos por habitantes. Logo, estas cidades também grande potencial de geração de lucro.
<br>
Se a empresa pretender expandir seu negócio, seria uma boa ideia considerar estes dois perfis de cidades. 
<br>

## 7. Em cidades com alto número de moradores em favela, deve-se atrair outro perfil de restaurante
Cidades com alto número de moradores em favela possuem itens caros. O que dificulta o consumo da população de baixa renda, isso gera um baixo valor total do pedido.
<br>
Esta questão é relevante, pois nestes lugares a empresa não está atingindo todo o potencial de clientes.
<br>
A Zomato poderia focar em atrair para seu app restaurantes locais com preços mais acessíveis, talvez focar estabelecimentos menores. Isso poderia atrair o público de classe média baixa.
<br>

## 8. 96% dos clientes compram a mesma categoria de alimentos
Como sugestão, a empresa poderia incluir, em seu app, uma coluna de subcategoria de comida melhorar o seu sistema de recomendação e a experiência de compra dos clientes.
<br>
Por exemplo, imagine um cliente que costuma comprar vários tipos hamburguer e refrigerantes. Ambos poderiam estar na categoria Fast Food. 
<br>
Se houvesse uma subcategoria para hamburguer e outra para refrigerante, a recomendação seria mais eficaz e não precisaria descer até o item. 
<br>
Além disso, ao navegar pela subcategoria "hambúrgueres", ele encontraria facilmente as opções que mais lhe agradam, sem precisar navegar por toda a categoria "Fast Food".
<br>

# Power Bi
Foi criado um Dashboard no Power Bi com o intuito de mostrar alguns tópicos da conclusão.E, a seguir, temos um vídeo mostrando o resultado.
<video src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Power%20Bi/Video_Powe_Bi_(versao_2).mp4"></video>


# Referências
**Census 2011 India**. Disponível em: [https://www.census2011.co.in/](https://www.census2011.co.in/)</a>  . Acesso em: 29 dez. 2023.
<br><br> 

India: GDP of major cities 2022.**Statista**. 2022.Disponível em: [https://www.statista.com/statistics/1400141/india-gdp-of-major-cities/](https://www.statista.com/statistics/1400141/india-gdp-of-major-cities/) . Acesso em: 28 dez. 2023.
<br><br>

**GeoIQ**. Disponível em: [https://geoiq.io/places/Koramangala/6P0l0H8Jya](https://geoiq.io/places/Koramangala/6P0l0H8Jya) . Acesso em : 25 dez. 2023. 
<br><br>

Mondol, Tapo. Do Indians order less food when eating out, but cook more at home? **Quora**. 2023. Disponível em: [https://www.quora.com/Do-Indians-order-less-food-when-eating-out-but-cook-more-at-home](https://www.quora.com/Do-Indians-order-less-food-when-eating-out-but-cook-more-at-home) . Acesso em: 31 dez. 2023.
<br><br>


MOHAN, N et al. Factors affecting frequency of eating out among Indians. International Conference on Communication and Signal Processing, 6 abr. 2016. Disponível em : [https://ieeexplore.ieee.org/abstract/document/7754477](https://ieeexplore.ieee.org/abstract/document/7754477 ) 
<br><br>


Population of Cities in India 2021. StatisticsTimes.com. 2021. Disponível em: [https://statisticstimes.com/demographics/country/india-cities-population.php]( https://statisticstimes.com/demographics/country/india-cities-population.php) . Acesso em: 27 dez. 2023.
<br><br>

   

 
