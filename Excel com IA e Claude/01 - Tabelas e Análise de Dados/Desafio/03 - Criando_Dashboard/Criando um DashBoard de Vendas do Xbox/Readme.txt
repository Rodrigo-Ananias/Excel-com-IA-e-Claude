Desafio "Criando um dashboard de vendas no Excel"

- Sobre o Projeto

O projeto atual pretende mostrar a criação de um Dashboard de vendas utilizando Excel. Foi utilizada técnicas de orientação ABCDE.

O que é o método ABCD? É um método de organização criado pelo professor da DIO.me, o Felipão da DIO. Esse método é aplicado para a criação de dashboard entre outras coisas.

A(ssets) - são todos os recursos de apoio, como a paleta de cores, ícones, imagens, vídeos e etc;
B(ases) - são os dados utilizados para gerar aquele dashboard ou outras medidas.
C(álculos) - são todos os cálculos utilizados (query, consulta etc), suas regras e scripts. É o meio de campo que processa dados para transformar dados em informações.
D(ashboards) - é o próprio painel visual.
E(xtra) - são os extras.




- Dados utilizados

A base de dados utilizados é a base.xlsx. Nela estão alocadas informações de vendas de assinaturas da XBOX Gaming. Em outras palavras, os dados utilizados visam apresentar o controle de assinaturas feito pela XBOX no seu ramo de games. 

- Instruções para a reprodução

Como reproduzir esse dashboard? Aplicando a metodologia ABCDE.

Antes, vamos compreender os dados. Na Pasta de Trabalho base.xlsx estão presentes 4 planilhas. Assets, Bases, Cálculos e Dashboards.

A planilha 1 são os Assets, nela estão os códigos das paletas de cores, logos, ícones e imagens. Essa é a aba onde estão todos os recursos de apoio visual que foram utilizados para a produção da dashboard.

A planilha 2 estão as Bases utilizadas, em outras palavras, estão os dados brutos divididos em linhas e colunas. É uma base de dados de assinaturas da XBOX gaming. Estão presentes 13 colunas, sendo Subscriber ID; Name; Plan; Start Date; Auto Renewal; Subscription Price; Subscription Type; EA Play Season Pass Price; Minecraft Season Pass; Minecraft Season Pass Price; Coupon Value e Total Value. 
Em suma, as colunas apresentadas retratam informações de assinaturas, renovação, valores e planos e outras coisas. Vale mencionar que os valores já estão convertidos em reais nessa planilha.

Na planilha 3, Cálculos, estão presentes todos os cálculos e medidas feitas. Por ser o mais extenso serão apresentado em um capítulo independente.

Por fim, a planilha 4, Dashboard, é o painel visual em si. Caso seja necessário, ele também será explicado em um capítulo próprio.

- Planilha 3 e 4, Cálculos e gráficos iniciais

Primeiro, transformaremos dados em informações. 

Uma informação é uma pergunta de negócio respondida através de alguma análise de dado específica.
Como eu respondo essa pergunta? Por meio de um cálculo (uma métrica específica).


Pergunta de Negócio 1 - Qual o faturamento total de venda de planos anuais (contendo todas as assinaturas agregadas)? Palavras-chaves: total de vendas, plano anual.


1 - Criação de uma Tabela Dinâmica nomeada tbl_anual_total . Temos 4 campos da Tabela Dinâmica. Para responder a pergunta acima, fizemos o seguinte

Campo Linhas (Subscription Type - somente annual);
Campo Valores (Soma de Total Value)
Campo Filtros ()
Campo Colunas ()

Resposta: R$ 7.663,00


Pergunta de Negócio 2 - Qual faturamento total de vendas de planos anuais, separado por auto renovação e não auto renovação? Palavra-chaves: total de vendas de planos anuais, auto renovação e não auto renovação.

Utilizamos a mesma Tabela Dinâmica e só alteramos os campos.

Campo Linhas (Subscription Type - somente annual; Auto Renewal - todos);
Campo Valores (Soma de Total Value)
Campo Filtros ()
Campo Colunas () 

ou 

Campo Linhas ( Auto Renewal - todos);
Campo Valores (Soma de Total Value)
Campo Filtros (Subscription Type - somente annual;)
Campo Colunas () 

Em ambos a resposta será R$1537,00 em auto renovação e R$217,00 no outro.

Pergunta de Negócio 3 - Total de Vendas de Assinaturas do EA Play? Palavras-chaves: total de vendas e assinatura do EA Play.

Duplicamos a tabela dinâmica tbl_total_anual e usamos os seguintes campos:

Campo Linhas ( Plan - todos);
Campo Valores (Soma de EA Play SeasonPrice)
Campo Filtros (Subscription Type - somente annual;)
Campo Colunas ()

Resposta: R$600,00 de vendas total.

Pergunta de Negócio 4 - Total de Vendas de Assinaturas do Minecraft Season Pass? Palavras-chaves: total de vendas, assinatura Minecraft.

Duplicamos a tabela dinâmica tbl_total_anual e usamos os seguintes campos:

Campo Linhas ( Plan - todos);
Campo Valores (Soma de Minecraft Season Pass Price )
Campo Filtros (Subscription Type - somente annual;)
Campo Colunas ()
	

2 - Criação de Gráficos

Inserimos um gráfico dinâmico e um segmentador de dados. Como?

Primeiro, apertamos na nossa tabela dinâmica e depois em Análise de Tabela Dinâmica. Depois, no menu Ferramentas, clicamos em Gráfico Dinâmico e selecionamos Barras agrupadas.
Para o segmentador, clicamos na tabela dinâmica, INSERIR, menu Filtros e selecionamos Segmentação de Dados e segmentamos por Subscription Type.

- 4 Planilha, Dashboard

Criar uma visualização vai além de deixar a tela bonita. A ênfase é na qualidade que aquela visualização se converte em uma informação clara e consumível. Ela deve servir ao seu propósito real, auxiliar humanos na tomada de decisões. Lembre-se do seu público-alvo e como adequar aquela informação àquele público.

As imagens utilizadas foram formatadas para não mover ou dimensionar com células.

- Recomendações de Leitura

"Não me faça pensar" de Steve Krug - ênfase em usabilidade.


