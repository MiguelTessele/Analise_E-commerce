# Projeto de Análise de Empresa  E-Commerce
<div style="display: flex; justify-content: space-between;"> <br>
<img width="1000" alt="netflix" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Capa.png">
  
# Sobre o Projeto:
O objetivo deste projeto é desenvolver painéis que demonstrem o cenário atual de vendas da empresa e o desempenho de seus produtos. O cliente solicitou que mantivéssemos o sigilo de sua marca; portanto, o logo da empresa foi excluído. Utilizamos uma base de dados que o cliente nos enviou em formato 'xlsx', com os dados requisitados para análise e possíveis insights. A primeira aba do dashboard irá abordar indicadores gerais da empresa, proporcionando uma visão macro das operações. Na segunda aba, serão analisados o faturamento anual, semestral e mensal, permitindo compreender a sazonalidade e os motivos de devoluções. Na terceira aba, iremos examinar os produtos mais vendidos, o retorno financeiro das marcas, além dos produtos mais devolvidos e seus respectivos motivos. Após feitas essas análises, partiremos para uma avaliação das lojas, onde iremos observar o retorno e os custos, identificando oportunidades de expansão e comparando o desempenho entre lojas físicas e online. Para concluirmos a análise com a base de dados fornecida, iremos observar e analisar o perfil dos clientes, incluindo faixa etária, gênero e comportamento de compra, para identificar oportunidades de atração de novos clientes.

Essa análise irá oferecer uma visão abrangente do negócio, ajudando a identificar oportunidades, áreas de melhoria e a reconhecer esforços bem-sucedidos. A identificação dos principais produtos, marcas e clientes permitirá a criação de estratégias mais direcionadas e eficazes para aumentar o faturamento e a lucratividade.

<br />

# Etapas do Projeto (DataOps)

• Perguntas de negócio;

• Mapeamento dos dados;

• Prototipação;

• ETL (Extração, Transformação e Carregamento);

• Descobertas e insights;

• Sugestões de decisão.

<br />

# Perguntas de Negócio

Com o objetivo de fornecer insights e soluções a partir dos dados fornecidos, foram levantadas algumas perguntas para entender a necessidade do negócio:

• Quais produtos apresentam maior volume de vendas e quais são suas respectivas margens de lucro?

• Quais são os produtos com maior taxa de devolução e qual é o motivo mais comum dessas devoluções?

• Como o desempenho de vendas varia por estação ou por mês? Existe um padrão sazonal evidente?

• Qual é o perfil dos nossos melhores clientes (faixa etária, localização, gênero)? Podemos criar campanhas para alcançar clientes com perfis semelhantes?

• Como varia a frequência de compras entre diferentes grupos de clientes? Podemos criar campanhas de fidelização para aumentar essa frequência?

• Quais regiões apresentam o menor desempenho e como podemos melhorar o alcance nessas áreas?

• Quais são os principais motivos das devoluções e como podemos reduzir essas ocorrências?

Após feitas as perguntas de negócio, as respostas fornecerão uma visão do comportamento dos clientes, produtos e do cenário atual da empresa, que se encontra em momento de expansão.


<br />

# Mapeamento dos Dados

Os dados foram disponibilizados em arquivos Excel (“Base Devoluções”, “Base Vendas – 2020”, “Base Vendas – 2021”, “Base Vendas – 2022”, “Cadastro Clientes”, “Cadastro Localidades”, “Cadastro Lojas”, “Cadastro Produtos”), contendo as dimensões de Clientes, Localidade, Lojas e Produtos, como mostra a imagem abaixo.

 <img width="500" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Base.png">


# Prototipação

Com base no entendimento do problema e nas necessidades dos indicadores que o cliente solicitou, foram desenvolvidas as telas de prototipação para o desenvolvimento dos dashboards. As telas servirão como guia para a construção dos dashboards finais, garantindo que todas as necessidades e objetivos identificados sejam atendidos. Foram introduzidos alguns indicadores com novas visões do negócio, pois o cliente está planejando uma expansão próxima. A ferramenta utilizada foi o Figma, permitindo visualizar uma prévia de como ficará a entrega final. Foi utilizado o Adobe Color para extrair o número HEX de cada cor.

<br />
<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Pag_1_.png"><h4>Protótipo página 1</h4>
</div>

<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Pag_2_.png">
  <h4>Protótipo página 2</h4>
</div>


<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Pag_3_.png">
  <h4>Protótipo página 3</h4>
</div>

<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Pag_4_.png">
    <h4>Protótipo página 4</h4>
</div>
<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Pag_5_.png">
  <h4>Protótipo página 5</h4>
</div>
<br />

# ETL (Extração, Transformação e Carregamento)

### Preparação dos dados

• A extração da base foi feita no Power Query;

• Limpeza de dados inconsistentes;

• Colunas com valores "null" foram excluídas pois não tinham relevância;

• As tabelas fato receberam um prefixo “f” e as dimensões um prefixo “d” para facilitar a distinção;

• Identificação e correção dos tipos de dados para garantir a criação de medidas precisas e um relacionamento consistente • entre as tabelas;

• Arredondamento das casas decimais (2 casas);

• As tabelas de vendas, originalmente separadas por ano, foram unificadas para possibilitar um relacionamento mais • consistente e análises anuais e históricas;

• Após o tratamento, os dados foram carregados e modelados no Power BI para a criação dos dashboards.

Abaixo estão alguns exemplos do processo de ETL, como estava antes e como ficou após a aplicação das transformações.

<br />
<div align="center">
  <h4>Tabela de Clientes antes do tratamento dos dados</h4>
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Tabela_Clientes_Antes.png">
</div>
<div align="center">
  <h4>Tabela de Clientes após o tratamento dos dados</h4>
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Tabela_Clientes_DPS.png">
</div>
<br />

Podemos observar que os dados continham inconsistências como:

• As colunas estão sem nomes, o que dificulta a interpretação dos dados;

• Os tipos das colunas estão errados, todas no mesmo formato (texto e números misturados);

• As duas primeiras linhas de todas as colunas estão com valores nulos;

• Os nomes das colunas estão na 3ª linha;

• Para melhor interpretação, foram substituídos os valores das colunas 'Gênero' e 'Estado civil', retirando as abreviações e adicionando as nomenclaturas completas.

<br />
<div align="center">
  <h4>Tabela de Vendas antes o tratamento dos dados</h4>
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Tabela_Vendas_Antes.png">
</div>
<div align="center">
  <h4>Tabela de Vendas após do tratamento dos dados</h4>
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Tabela_Vendas_DPS.png">
</div>
<br />

Podemos observar que os dados continham inconsistências como:

• As colunas estão sem nomes, o que dificulta a interpretação dos dados;

• Os tipos das colunas estão errados, todas no mesmo formato (texto e números misturados);

• Os dados sobre as vendas estavam separados por anos, dificultando a criação de uma linha temporal. A resolução foi unificar as tabelas.


# Dashboard Interativo

Com os dados devidamente organizados e coerentes, partimos para a elaboração de visualizações com dados estatísticos, que servirão como base para responder às questões propostas inicialmente. Foi necessário desenvolver medidas utilizando fórmulas DAX para melhor analisar os dados e extrair insights.

- [Clique aqui para visualizar o dashboard de maneira interativa](https://app.powerbi.com/links/5LSdfFYlMi?ctid=f5a6833e-3f93-41ac-8092-ee06a0910899&pbi_source=linkShare)
<br />

<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Analise_Geral.png">
</div>
<br />
<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Vendas_Devolucoes.png">
</div>
<br />
<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Marcas_Produtos.png">
</div>
<br />
<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Marcas_Produtos.png">
</div>
<br />
<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Lojas.png">
  </div>
 <br /> 
<div align="center">
  <img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Clientes.png">
</div>
<br />

# Análises e Insights

<img width="1000" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Insights.jpeg">

Após a finalização do dashboard, foi realizada uma análise descritiva, na qual foram observados vários insights. Irei citar alguns, separados pelo nome das páginas para melhor entendimento:

**Análise Geral**

• O faturamento mensal apresenta crescimento constante até maio, atingindo um pico em junho (186 milhões);

• A margem mensal varia de 74,3% a 75,7%, apresentando um pico em junho, que pode estar relacionado ao tipo de produto vendido no período;

• A "Loja Catalog" lidera o faturamento com 105 milhões, enquanto outras lojas, como "Loja Yerevan", têm desempenho significativamente menor (8 milhões);

• A Apple é a marca líder em faturamento (444,9 milhões), seguida por outras marcas como Asus (144,4 milhões).

**Vendas e Devoluções**

• O faturamento teve um crescimento expressivo de 218 milhões em 2020 para 598 milhões em 2021 (174% de aumento). Em 2022, o faturamento aumentou para 795 milhões, embora o ritmo de crescimento tenha diminuído (18%). É importante ressaltar que em 2022 possuímos os dados até junho;

• Houve um aumento constante nas devoluções de 2020 (7,5 milhões) para 2022 (20,3 milhões), indicando um problema recorrente de qualidade. A taxa de devolução está em 7,3%, com "Produto com Defeito" sendo o principal motivo;

• O faturamento mensal mostra flutuações consideráveis, com janeiro sendo um dos meses mais baixos (20 milhões) e junho um dos mais altos (24 milhões). As devoluções, mantêm uma média estável, sem uma queda significativa mostrando que a consistência das devoluções indica que o problema não está relacionado a fatores sazonais, mas sim a problemas contínuos de qualidade ou atendimento;

• O ticket médio se manteve estável em torno de 61 mil ao longo dos anos, com um número total de pedidos de 25 mil. Isso mostra um comportamento de compra consistente, sem grandes oscilações em valor.

**Marcas e Faturamento**

• Algumas marcas, como Vaio e Compaq, apresentam um faturamento consideravelmente menor, abaixo de 10 milhões;

• O "Mouse sem fio MO251 2.4 Ghz - Preto" é o produto mais vendido (7.967 unidades), mas também apresenta o maior número de devoluções (155 unidades);

• Os Produtos periféricos, como mouses e teclados, têm alto volume de vendas, mas também são os produtos mais devolvidos;

• É importante observar que produtos de valor agregado mais alto, como notebooks, têm melhores margens e menos devoluções.

**Lojas**

• Existem 306 lojas distribuídas em quatro continentes, com maior concentração na América do Norte (209 lojas). Europa, Ásia, e Oceania têm uma presença consideravelmente menor;

• As lojas físicas possuem um custo muito maior do que as lojas online, mas seu impacto no faturamento justifica esse investimento, geram a maior parte do faturamento, com 1,273 bilhões, enquanto as lojas online têm um desempenho menor;

• Lojas como Loja Catalog têm altos custos, mas também apresentam alto faturamento e lucro. Já outras lojas apresentam custos elevados sem alcançar um bom faturamento;

• A distribuição dos tickets médios é relativamente equilibrada entre as lojas principais, sugerindo um bom trabalho em direcionar os consumidores para produtos de valor.

**Clientes**

• Há 18 mil clientes cadastrados, dos quais 17 mil são ativos, representando 96% da base. Isso indica uma boa retenção e envolvimento da maioria dos clientes;

• O público mais jovem (18-25 anos) tem menor representatividade, indicando uma oportunidade de expansão para atrair essa faixa etária;

• O gênero dos clientes está bem equilibrado, com 9.011 homens e 9.137 mulheres, o que indica uma distribuição uniforme entre ambos os gêneros;

• A frequência média de compra é de 53 dias, enquanto o ticket médio é de 61 mil. Isso indica que, embora os clientes tenham um intervalo conside rável entre compras, o valor gasto em cada compra é significativo.

# Recomendações ao tomador de decisão

<img width="1000" alt="Imagem dados" src="https://github.com/MiguelTessele/Analise_E-Commerce/blob/main/Sugestoes_negocios.png">
 
Com base nos insights obtidos, sugerimos algumas alternativas aos dirigentes para que a empresa possa aprimorar seus resultados e desenvolver a expansão de suas lojas, separadas pelo nome das páginas para melhor entendimento.

**Análise Geral**

• Criar campanhas promocionais para os períodos de baixa demanda (ex.: julho e agosto), para suavizar a queda de faturamento pós-pico;

• Identificar quais produtos ou campanhas contribuíram para a margem mais alta em junho e replicar estratégias similares em outros meses;

• Realizar um estudo de benchmarking com as lojas de melhor desempenho, como a Loja Catalog, analisando o portfólio de produtos, estratégias de vendas para identificar práticas que possam ser aplicadas em lojas com menor faturamento;

• Diversificar o portfólio para reduzir a dependência da marca Apple, incentivando a venda de outras marcas que também apresentam boas margens, como Asus. Além disso avaliar a continuidade dos produtos de  marcas com baixo desempenho ou criar promoções específicas para reduzir estoques dessas marcas.

**Vendas e Devoluções**

• Desenvolver campanhas específicas para o segundo semestre, como promoções de fim de ano e campanhas da Black Friday para manter o ritmo de vendas;

• Melhorar a experiência do cliente com descrições claras dos produtos, vídeos explicativos, e suporte técnico para diminuir o número de devoluções por arrependimento ou problemas simples e implementar um programa rigoroso de controle de qualidade com os principais fornecedores, visando reduzir defeitos e consequentemente, devoluções;

• Revisar o controle de qualidade, especialmente nos produtos que têm alta taxa de devolução e implementar métricas de controle de qualidade mais rigorosas, como auditorias nos produtos mais vendidos e acompanhamento do feedback dos clientes;

• Incentivar a venda de produtos complementares e pacotes promocionais para aumentar o ticket médio. Podemos tambem explorar a segmentação dos clientes para campanhas personalizadas que incentivem compras de valor maior oferecendo descontos exclusivos  para compras acima de determinado valor pode ajudar a aumentar o ticket médio.

**Marcas e Faturamento**

•  Avaliar a continuidade dos produtos das marcas com baixo desempenho. Em caso de baixa demanda, produtos dessas marcas poderiam ser descontinuados ou  vendidos com promoções agressivas para liberar  espaço no estoque;

• Realizar melhorias na qualidade do "Mouse sem fio MO251" ou ajustar a descrição do produto para alinhar as expectativas dos clientes e reduzir as devoluções;

• Focar em campanhas de marketing para promover produtos com alta margem e baixa taxa de devolução, como o "Notebook Asus ROG Zephyrus Duo". Isso pode maximizar a rentabilidade e minimizar problemas com  devoluções;

•  Criar campanhas exclusivas para marcas como Acer, Dell, e HP, destacando suas vantagens competitivas (como melhor custo-benefício) para atrair consumidores e melhorar a margem de lucro geral.

**Lojas**

• Avaliar a possibilidade de expandir para regiões sub-representadas, como Ásia e Oceania, que possuem menos lojas e, consequentemente, menor faturamento;

• Melhorar a integração entre lojas físicas e online com estratégias como "compre online e retire na loja". Isso ajudaria a aumentar as vendas online e melhorar a experiência do cliente;

• Utilizar as lojas de maior custo-benefício como referência para reestruturar as lojas menos rentáveis, incluindo a revisão das lojas de baixo desempenho e com custo elevado;

• Promover campanhas sazonais específicas que incentivem a compra de produtos com maior valor agregado, especialmente em lojas onde o ticket médio é mais baixo.

**Clientes**

• Desenvolver uma campanha de reativação para os clientes inativos, oferecendo benefícios como descontos ou promoções exclusivas para incentivá-los a oltarem a comprar criando um programa de fidelidade que recompense os clientes por sua atividade contínua, mantendo-os engajados e ativos;

• Desenvolver estratégias de marketing voltadas para o público jovem (18-25 anos), como presença em redes sociais específicas para essa faixa (TikTok, Instagram), além de promoções focadas  em produtos que sejam mais atraentes para esse público;

• Criar campanhas específicas de marketing direcionadas ao estado civil dos clientes, como promoções de "Dia dos Namorados" para clientes solteiros e "Descontos em Família" para clientes casados;

• Desenvolver um programa de recompensas para incentivar compras mais frequentes, reduzindo o intervalo médio entre elas, como cupons de desconto após uma compra ou pontos que acumulam para futuras compras.
