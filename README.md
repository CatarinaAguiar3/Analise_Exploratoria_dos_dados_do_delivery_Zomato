<Img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Banner_para_README4.png" >

<div>
<h2>Tabela de Conteúdo</h2> 
  <a href="#">Introdução da Análise Exploratória</a> <br>
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
 <a href="#referências">Referências</a><br>


# Introdução
<div style="text-align: justify;">
A análise descritiva será divida em duas partes: <b>Análise descritiva geral</b> e <b>Regra de Associação</b>.
<br><br>
A <b>Análise descritiva geral</b> será dividida em 6 tópicos: <b>Resumo Estatístico das variáveis, Análise Preço e Quantidade, Análise Índia, Rating, Análise do Perfil dos clientes e Análise dos dias da semana.</b>
<ul>
<li><b>Resumo Estatístico das variáveis:</b>calculo de medidas estatísticas como a média. O objetivo é entender a distribuição dos dados. Além disso, também será calculado a frequência dos valores únicos.</li>
<li><b>Análise Preço e Quantidade:</b>o objetivo é investigar as colunas relacionadas a preço e quantidade, por exemplo, preço do item e quantidade vendida.</li>
<li><b>Análise Índia:</b>analisar como dados geoeconômicos da Índia podem ser relacionar com as variáveis da tabela.</li>
<li><b>Rating:</b>descobrir mais sobre como a classificação média dos restaurantes e o número de avaliações se relacionam com as outras colunas da tabela.</li>
<li><b>Análise do Perfil dos clientes:</b>entender como informações do cliente pode estar associada ao seu comportamento de compra.</li>
<li><b>Análise dos dias da semana:</b>separar as vendas por dia da semana.</li>
</ul>

<br><br>
Na <b> segunda parte será feita a Regra de associação</b> usando dois algoritmos: Apriori e FP-Growth.Em seguida, será feita a análise das regras geradas, além da <b>associação de todas as regras geradas ao user_id.</b>
</div>

# Análise Descritiva Geral
## Resumo Estatístico das variáveis

### **1. Resumo Tamanho da Família** 
O mínimo é 1 e o máximo é 6. A média é 3,2 e o valor 3 é o que mais aparece. 
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.1_Tabela.png" width="50%">
<br>

### **2.Resumo Valor Total do Pedido (em USD)** 
A média é 39.75 e a mediana é 15.
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.2_Tabela.png" width="25%">
<br>

### **3.Resumo Quantidade de itens encomendados**
A média é 5.36 e a mediana é 2. E, 45% das pessoas compram 1 item.
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.3_Tabela.png" width="25%">
<br>

### **4.Resumo de city**
Existem 58 valores para cidades. Porém 3 cidades estão separadas em bairros. Então o número de cidades em absoluto é um pouco menor, 44. 
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.4_Tabela.png" width="40%">
<br>

### **5.Resumo Classificação média do restaurante**
As avaliações vão de 0 à 5, sendo 0 a pontuação de restaurantes que não foram avaliados. Na limpeza dos dados foram retirados os restaurantes sem avaliação.
<br>
Após isso, o valor mínimo de avalição é 1.3 e o máximo é 5. A média é 3.8 e a mediana é 3.9.
<br> 
A proporção de notas está bem distribuída. Sendo 4 a nota com maior frequência.
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.5_Tabela.png" width="50%">
<br>

### **6.Resumo Custo médio por pessoa para uma refeição no restaurante**
A média é de 3.7 , a mediana é de 3.6 e o máximo é de 21.6. Estes valores são mais baixos que os preços de cada item. Além disso, 22% dos restaurantes tem o custo médio por pessoa de 2.4 Dóllares.
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.6_Tabela.png" width="50%">
<br>

### **7.Resumo Tipo de cozinha oferecida pelo restaurante** 
Existem 603 tipos de restaurante, porém alguns estão combinados. Se fosse retirado o nome depois da vírgula, quantidade de tipos de restaurante cairia para 70. 
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.7_Tabela.png" width="70%">
<br>

### **8.Resumo ocupação do usuário**
Existem apenas 4 tipos de ocupação estudante (52%), empregado (31%), autônomo (13%) e dona de casa (2%).
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.8_Tabela.png" width="40%">
<br>

### **9.Resumo Renda mensal do usuário**
A maior parte dos clientes não possuem renda (47%), provavelmente, são os mesmos clientes que estudam.
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.9_Tabela.png" width="40%">
<br>

### **10.Resumo Escolaridade do usuário** 
A maior parte dos clientes tem graduação (46 %) ou Pós graduação (43%).
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.10_Tabela.png " width="40%">
<br>

### **11.Resumo Idade**
Os clientes tem uma faixa etária de 18 e 33 anos. Sendo que na média, eles tem 24 anos. 
<br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.11_Tabela.png" width="20%">
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
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.12_Grafico.png" width="50%">
<br>

###  **13.Qual a Distribuição de preço de alimentos vegetarinos?**
A média de preço é de 2.3 Dólares
<br> 
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.13_Tabela.png" width="20%">
<br>

### **14.Qual a Distribuição de preço de alimentos NÃO vegetarinos?**
A média de preço é de 3.09 Dólares
<br> 
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.14_Tabela.png " width="20%">
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
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.15_Grafico.png" width="80%">
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
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.16_Grafico.png" width="80%" >
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
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.17_Grafico.png" width="80%" >
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
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.18_Grafico.png" width="80%" >
<br><br>
Foi feito no Power Bi um mapa das cidades com mais vendas
<center>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.18_mapa_cidades_com_mais_n%C2%BA_pedidos.png" width="70%" >
<br><br>

</center>

### **19. Ranking das 10 categorias de restaurante com menores preços (custo médio por refeição)** 
**OBS:** Os preços são calculados em Dóllar Americano
<br><br>
As categorias com o menor custo médio por refeição são Italian-American ,  Rajasthani , Juices e Café.
Rajasthani é uma culinária do noroeste da Índia.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.19_Grafico.png" width="80%" >
<br><br>

### **20. Quais as cidades com o custo médio de refeição por pessoa mais caro?** 
As cidades de Bangalore e Ahmedabad possuem o custo por refeição mais caro. Elas também são as cidades com os maiores números de pedidos.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.20_Grafico.png" width="80%" >
<br><br>
<center>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.20_card_cidades_custo_mais_caro.png" width="70%">
</center>

### **21. Quais as cidades com o custo médio de refeição por pessoa mais barato?** 
As cidades do nordeste são as que tem o custo por refeição mais barato. Seguidas de algumas cidades ao sul.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.21_Grafico.png" width="80%" >
<br><br>

O mapa a seguir foi feito no Power Bi
<br>
<center>
<img src= "https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.21_mapa_cidades_com_custo_medio_de_refeicoes_por_pessoa_maiores_barato.png" width="70%" >
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
Fontes: <a href="https://pt.wikipedia.org/wiki/Economia_da_%C3%8Dndia">Wikipedia</a> e <a href="https://www.investindia.gov.in/pt-br/great-places-for-manufacturing-in-india">Investindia.gov.in</a>]
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.22_Grafico.png" width="80%" >
<br><br>

O mapa a seguir foi feito no Power Bi
<br>
<center>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.22_mapa_cidades_com_maiores_valores_totais_por_pedido_(sales_amount)1.png" width="70%" >
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
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.23_Grafico.png" width="80%" >
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

<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.24_card_city3.png" width="50%">
Fonte:<a href="https://geoiq.io/places/Koramangala/6P0l0H8Jya">geoIQ</a>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.24_Grafico.png" width="80%" >
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
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Tabela_An%C3%A1lise_%C3%8Dndia_infoma%C3%A7%C3%B5es_geoecon%C3%B4micas.png" width="80%" >
<br><br>

###  **25. Relação entre o preço por item e porcentagem de residentes que moram em favela** 
Em ambas as correlações, o p-valor foi baixo. Portanto a associação entre as variáveis é significativa. Já os coeficientes foram positivos e baixos.
<br><br>
Isso indica que existe associação entre o preço por item e a porcentagem de residentes que moram em favelas. Esta associação é positiva e fraca.
<br><br>
Portanto, cidades com altos preços por item, também possuem alto número de favelas. Este resultado pode indicar que as cidades indianas tem grande desigualdade econômica e também explica o porque de 45% das pessoas desta base de dados comprarem apenas 1 item (visto na pergunta 3)
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.25_Correlacoes.png" width="50%" >
<br><br>

### **26. Relação entre custo médio da refeição e porcentagem de residentes que moram em favela** 
Em ambas as correlações, o p-valor foi muito baixo e a correlação fraca. A Correlação de Pearson resultou em um valor positivo, enquanto a Correlação de Spearman foi negativa.
<br>
Portanto, há envidência <mark>**de uma relação entre o custo médio por refeição por cidade e a porcentagem de moradores de favela por cidade. Porém, a forma desta relação não é clara.**</mark>
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.26_Correlacoes.png" width="50%" >
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.26_Grafico.png" width="80%" >
<br><br>

### **27. Relação entre a porcentagem de residentes que moram em favela e a média do valor total de pedidos (sales_amount_usd)** 
O p-valor das duas correlações foi significativo.
E, ambos os coeficientes indicam que há uma relação negativa entre valor total do pedido e nº de moradores de favela, de modo que quando uma variável aumenta.
<br><br>
De modo geral, pode-se dizer que <mark>**há associação negativa entre o valor total do pedido e nº de moradores de favela.**</mark>. De modo que quando uma variável aumenta, a outra diminui.De modo que quando uma variável aumenta, a outra diminui. <br><br>
Este resultado faz sentido, pois um grande número de moradores em favela pode ser um indicativo de pobreza, logo, as pessoas não tem muito dinheiro disponível para gastar com lanche.
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.27_Correlacoes.png" width="50%" >
<br><br>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.27_Grafico.png" width="80%" >
<br><br>

###  **28. Quais as 15 cidades com os maiores pedidos por habitante?** 
Para responder esta pergunta será feita a contagem do número de pedidos por cidade. Em seguida, será carregada a tabela com a população por cidade. E depois , será feita a união das duas tabelas. 
<br><br>
Então, será feito o cálculo a seguir:
<br><br>
<center>
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.28_numero_de_pedidos_por_habitante1.png" width="60%">
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
<img src="https://github.com/CatarinaAguiar3/Analise_Exploratoria_dos_dados_do_delivery_Zomato/blob/main/Imagens/Analise_Descritiva_Geral/Q.28_Grafico.png" width="80%" >
<br><br>

###  **29. Qual a correlação entre o número de pedidos por cidade e o tamanho da população?**
Existe uma correlação positiva e <b>forte</b> entre tamanho da população e número de pedidos. Além disso, o p-valor é  muito pequeno, logo, está associação linear é estatisticamente significativa.
<br><br>
Em geral,  <mark>**há uma associação entre número de pedidos e tamanho da população.**</mark> 
<br><br>
<img src="" width="80%" >
<br><br>

### **30. Distribuição da Religião Predonominante nas cidades da base de dados. E o tipo de comida com mais pedidos em cada cidade.** 
O mapa a seguir foi feito no Power Bi usando Tabela <code>nome_city5</code> criada no início da secção <code> Análise Índia</code>
<br>
É possível observar no mapa que a religião Predominante é o Hinduísmo, seguido do Islamismo. Isso é importante, pois <mark>**a religião pode influenciar os hábitos alimentares, por exemplo, com restrição a algum alimento.**</mark>
<br><br>
Além disso, <mark>**cada religião tem suas datas festivas que podem influenciar as vendas neste período.**</mark>
<br>
<img src="../Imagens/Analise_Descritiva_Geral/Q.30/Q.30_mapa_distrib_religiao_por_cidade2.png" width="100%">

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
<img src="" width="80%" >
<br><br>

## **Classificação média dos restaurantes**
### **32. Existe alguma correlação entre a classificação média do restaurante e o número de avaliações?** 
A correlação de Pearson foi de 0.14 e o p-valor foi muito baixo. Indicando que há uma associação linear entre as duas variáveis, porém esta associação é fraca.
<br><br>
Já a correlação de Pearson foi de 0.21 e o p-valor também foi muito baixo. O indicando que há uma associação positiva e moderada entre as variáveis.
<br><br>
Pode-se concluir que <b>há associação entre as variáveis</b>. De modo que,  quando a classificação média do restaurante, o número de avaliações também aumenta. Entretanto, esta associação não implica em causalidade, é possível que outros fatores influenciem esta relação.
<br><br>
<img src="" width="50%" >
<br><br>

### **33. Existe correlação entre a classificação do restaurante e o custo médio por pessoa?** 
Em ambas as correlações o resultado foi positivo e o p-valor foi muito baixo. Indicando que existe associação entre associação entre as variáveis. De modo, que um aumento da classificação do restaurante está associado a um aumento no custo médio. 
<br><br>
<img src="" width="50%" >
<br><br>

### **34. Qual a correlação entre o preço médio da refeição e a classificação do restaurante?** 
As correlações deram um valor positivo e baixo. E, os p-valor foram significativos. Portanto, existe uma associação positiva (mas fraca) entre o preço médio da refeição e a classificação do restaurante.
<br><br>
<img src="" width="50%" >
<br><br>

###  **35. Quais os tipos de restaurantes com a pontuação mais alta?**
As comidas Paan , Ice Cream, Waffle e Coastal possuem  as pontuações mais altas.
<br><br>
<img src="" width="50%" >
<br><br>

###  **36. Qual a classificação média das 10 categorias de restaurantes com preço médio mais alto?** 
Foi analisado os 10 tipos de restaurantes com maiores os preços mais altos. A partir daí, foi encontrado a classificação média deles.
<br><br> 
Não há uma relação clara entre as duas variáveis. Por exemplo, Japonese é o tipo de restaurante com o maior preço e também possui uma classificação alta. Entretanto, Middle Eastern tem um dos preços mais baixos e também possui uma classificação alta.
<br><br>
<mark>**Pode-se afirmar que os tipos de restaurantes com maiores preços têm boas classificações (acima de 3.8)**</mark> 
<br>
<img src="../Imagens/Analise_Descritiva_Geral/Q.36/Q.36_tabela_preco_e_classificacao1.png" width="80%">
<br><br>
<img src="" width="50%" >
<br><br>
